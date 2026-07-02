rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /valora_bank_data/central_state {
      allow read, write: if true;
    }
    match /valora_bank_users/{userId} {
      allow read, write: if true;
    }
    match /valora_bank_notifications/{notificationId} {
      allow read, write: if true;
    }
    match /valora_bank_transactions/{transactionId} {
      allow read, write: if true;
    }
  }
}
