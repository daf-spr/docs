---
section: libraries
description: MFA Widget language file example (English)
---

# MFA Widget: Language file example (English)
```json
{
  "defaults": {
    "iddleHelpUrl": "#",
    "rememberBrowserCheckbox": "Remember this browser",
    "title": "Login to {tenantName}"
  },
  "downloadApp": {
    "headerText": "Download Auth0 Guardian for free:",
    "pushEnrollmentAction": "I've already downloaded it",
    "smsAndTotpEnrollmentActions": "I'd rather use <sms>SMS</sms> or <ga>Google Authenticator</ga>",
    "totpEnrollmentActions": "I'd rather use <ga>Google Authenticator</ga>"
  },
  "pushAuth": {
    "pushSent": {
      "useTotpFallback": "If you haven't received the notification,<br></br>just <manualInput>enter the code</manualInput> manually."
    },
    "pushTimeout": {
      "resendAction": "Resend push notification",
      "timeoutText": "Didn't receive the push notification?",
      "useRecoveryCode": "Lost your device? <recovery>Use the recovery code</recovery>",
      "useTotpFallback": "<manualInput>Enter the code manually</manualInput>"
    }
  },
  "totpAuth": {
    "codePlaceholder": "Enter the 6-digit code",
    "headerText": "Get a verification code from the Google Authenticator (or similar) app:",
    "useRecoveryCode": "Lost your device? <recovery>Use the recovery code</recovery>"
  },
  "smsAuth": {
    "codePlaceholder": "Enter the 6-digit code",
    "headerText": "Enter the 6-digit code we've just sent to your phone.",
    "useRecoveryCode": "Lost your device? <recovery>Use the recovery code</recovery>"
  },
  "guardianTotpAuth": {
    "codePlaceholder": "Enter the 6-digit code",
    "headerText": "Get a verification code from the Auth0 Guardian app."
  },
  "recoveryCodeAuth": {
    "codePlaceholder": "Enter your code here",
    "headerText": "We will generate a new recovery code<br />once you've logged in:"
  },
  "pushEnrollment": {
    "headerText": "Scan this code with Auth0 Guardian:"
  },
  "enrollmentCongrats": {
    "congrats": "Congratulations, you are all set.<br />In future when logging in you'll want your device handy.",
    "continueButtonText": "Continue"
  },
  "reportRecoveryCode": {
    "confirmationLabel": "I have safely recorded this number",
    "headerText": "In the event that you need to login without your device you'll need a recovery code. Take a note and keep this somewhere safe:"
  },
  "generalError": {
    "errorsRecoveryHelp": {
      "default": "Looks like something went wrong.<br />Please try logging in again from the application.",
      "globalTransactionExpired": "The login was not successful.<br />Please try again.",
      "guardianInvalidNonce": "Please try logging in again from the application.",
      "guardianInvalidToken": "Please try logging in again from the application.",
      "invalidLoginTokenStatus": "Please try logging in again from the application.",
      "loginTokenInvalidSignature": "Please try logging in again from the application.",
      "loginTokenTransactionExpired": "Please try logging in again from the application."
    }
  },
  "smsEnrollmentConfirm": {
    "codePlaceholder": "Enter the 6-digit code",
    "headerText": "In order to confirm enrollment we need to confirm your phone. Please enter the received code."
  },
  "totpEnrollment": {
    "codePlaceholder": "Enter your passcode here",
    "headerText": "Scan this QR code with Google Authenticator (or similar) app:"
  },
  "smsEnrollmentAddPhoneNumber": {
    "headerText": "Please enter your phone<br />in order to enroll.",
    "phoneNumberLabel": "A code will be sent to this number:",
    "phoneNumberPlaceholder": "Your phone number"
  },
  "authCongrats": {
    "congrats": "We have verified your identity. Redirecting...",
    "congratsNoRedirect": "We have verified your identity.",
    "continueButtonText": "Continue"
  },
  "errorMessages": {
    "alreadyEnrolled": "You are already enrolled, cannot enroll again",
    "authMethodDisabled": "The specified authentication method is disabled",
    "connectionError": "Looks that we cannot contact our server. Please check your internet connection and retry.",
    "default": "Looks that something went wrong. Please retry.",
    "defaultRequest": "Looks that we found a problem contacting our server. Please retry.",
    "enrollmentConflict": "Seems that you have already enrolled. Try logging in again from the application.",
    "enrollmentMethodDisabled": "The specified enrollment method is disabled",
    "enrollmentNotFound": "We couldn't find your enrollment. You've probably started enrollment from another device. Finish it there or try logging in again from the application.",
    "enrollmentTransactionNotFound": "The mfa enrollment transaction is not active or has expired. Please try again.",
    "errorSendingPushNotification": "We found and error sending your PR. Please try again.",
    "errorSendingPushNotificationManualFallback": "We could not send the push. Please enter the code manually.",
    "errorSendingSms": "We found and error sending your code. Please try again in a few seconds.",
    "errorSendingSmsManualFallback": "We could not send the sms. Please try the recovery code.",
    "featureDisabled": "This module is currently disabled.",
    "featureDisabledByAdmin": "This module was disabled by the admin.",
    "fieldRequired": "Please fill out required field.",
    "globalTransactionExpired": "Your login attempt has timed out.",
    "guardianInvalidNonce": "There was a problem authenticating your request origin. Have you started too many parallel logins?",
    "guardianInvalidToken": "There was a problem validating authentication request format.",
    "insufficientScope": "Seems that you are not authorized to perform this action.",
    "invalidBearerFormat": "Seems that you are not authorized to perform this action.",
    "invalidLoginTokenStatus": "Unexpected state validating your request.",
    "invalidOtp": "Seems that your code is not valid, please check and retry.",
    "invalidOtpFormat": "OTP Code must have 6 numeric characters",
    "invalidPhoneNumber": "Seems that your phone number is not valid. Please check and retry.",
    "invalidRecoveryCode": "Seems that your recovery code is not valid. Please check and try again.",
    "invalidRecoveryCodeFormat": "Recovery code must have 24 alphanumeric characters",
    "invalidToken": "Seems that you are not authorized to perform this action.",
    "loginRejected": "Auth has been rejected. Try again.",
    "loginTokenInvalidSignature": "We cannot verify who seems to be the issuer for this request",
    "loginTokenTransactionExpired": "Your authentication request is expired. Is your connection slow?",
    "loginTransactionNotFound": "Seems that your device has taken too long to login. Please try again.",
    "noMethodAvailable": "There is currently no authentication method available.",
    "noPublicKeyAvailable": "We cannot verify your identity. Contact tenant admin.",
    "pnEndpointDisabled": "Seems that we cannot deliver messages to your cell phone. Please try again.",
    "pushNotificationNotConfigured": "Seems that enrollment was not finished. Please try logging in again from the application.",
    "pushNotificationWrongCredentials": "Seems that your device credentials are outdated. Please re-enroll your device or wait for them to be updated.",
    "smsNotConfigured": "You cannot use this module because you've enrolled with a different one.",
    "socketError": "We cannot connect to real time channel.",
    "tooManyPn": "You have exceed the amount of push notifications per minute. Please wait and try again.",
    "tooManyPnPerTenant": "There are too many push requests right now. Wait some minutes and try again.",
    "tooManySms": "You have exceed the amount of sms per hour. Wait some minutes and try again.",
    "tooManySmsPerTenant": "There are too many SMSs right now.  Wait some minutes and try again."
  },
  "successMessages": {
    "auth": "We have successfully verified your identity. Redirecting...",
    "pushSent": "We've sent a push to: {enrollmentName}",
    "smsSent": "We've sent an sms to: {phoneNumber}"
  },
  "infoMessages": {
    "iddle": "Can we help you?<br></br><iddleHelp>Click here to learn more</iddleHelp>"
  }
}
```
