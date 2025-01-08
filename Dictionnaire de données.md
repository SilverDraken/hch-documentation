
### 1.`Client` 

|Champ|Type|Description|
|---|---|---|
|`name`|`string`|Nom du client|
|`address`|`string`|Adresse du client|
|`email`|`string`|Adresse email du client|
|`phoneNumber`|`string`|Numéro de téléphone|

---

### 2.`Intervention`

|Champ|Type|Description|
|---|---|---|
|`id`|`string`|Identifiant unique de l'intervention|
|`type`|`string`|Type d'intervention|
|`createdDate`|`date`|Date de création|
|`dateOfIntervention`|`date`|Date prévue de l'intervention|
|`bikeModel`|`string`|Modèle du vélo concerné|
|`client`|`Client`|Document intégré représentant un client|
|`zone`|Référence à `Zone`|Zone où se déroule l'intervention|
|`technician`|Référence à `User`|Technicien assigné à l'intervention|
|`time`|`string`|Heure de l'intervention|
|`length`|`int`|Durée de l'intervention (en minutes)|

---

### 3.`User`

|Champ|Type|Description|
|---|---|---|
|`id`|`string`|Identifiant unique de l'utilisateur|
|`username`|`string`|Nom d'utilisateur|
|`email`|`string`|Adresse email|
|`password`|`string`|Mot de passe (haché)|
|`role`|`string`|Rôle de l'utilisateur (ex. Admin, Technicien)|
|`assignedZones`|Référence à `Zone[]`|Zones assignées à l'utilisateur|

---

### 4.`Zone`

|Champ|Type|Description|
|---|---|---|
|`id`|`string`|Identifiant unique de la zone|
|`name`|`string`|Nom de la zone|
|`description`|`string` (nullable)|Description de la zone|
|`color`|`string`|Couleur associée à la zone|
|`geometry`|`hash` (array)|Informations géométriques de la zone|
|`technician`|Référence à `User`|Technicien assigné à la zone|

---
