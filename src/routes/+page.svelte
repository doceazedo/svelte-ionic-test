<script lang="ts">
	import { alertController } from 'ionic-svelte';

	const showAlert = async () => {
   const alert = await alertController.create({
          header: 'Alert',
          subHeader: 'Important message',
          message: 'This is an alert!',
          buttons: ['OK'],
        });
   alert.present();
	}
</script>

<ion-header>
	<ion-toolbar>
		<ion-title>Very cool Ionic app 😎</ion-title>
	</ion-toolbar>
</ion-header>

<ion-content class="ion-padding">
  <ion-card>
		<ion-card-header>
			<ion-card-subtitle>Great success!!</ion-card-subtitle>
			<ion-card-title>Welcome to your app!</ion-card-title>
		</ion-card-header>

		<ion-card-content>
			Thank you for using this starter. Click buttons below to open these guides (will
			open in new window). Don't forget to open DevTools to see this app in mobile mode. Happy coding!!!
		</ion-card-content>
	</ion-card>

	<ion-list>
		<ion-item>
			<ion-label>Testar alerta uwu</ion-label>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<ion-button
				on:click={showAlert}
				fill="outline"
				slot="end">Click me</ion-button
			>
		</ion-item>
		<ion-item>
			<ion-label>Visit Ionic Showcase app with sourceviewer</ion-label>
			<ion-button href="https://ionicsvelte.firebaseapp.com/" target="_new" fill="outline" slot="end"
				>View</ion-button
			>
		</ion-item>
		<ion-item>
			<ion-label>Visit Ionic component docs</ion-label>
			<ion-button
				href="https://ionicframework.com/docs/components"
				target="_new"
				fill="outline"
				slot="end">View</ion-button
			>
		</ion-item>
		<ion-item>
			<ion-label>Visit Svelte Kit docs</ion-label>
			<ion-button
				href="https://kit.svelte.dev/docs/introduction"
				target="_new"
				fill="outline"
				slot="end">View</ion-button
			>
		</ion-item>
		<ion-item>
			<ion-label>Visit Svelte docs</ion-label>
			<ion-button href="https://svelte.dev/docs" target="_new" fill="outline" slot="end"
				>View</ion-button
			>
		</ion-item>
	</ion-list>
</ion-content>