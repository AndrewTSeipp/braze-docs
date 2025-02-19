---
nav_title: Aperçu
article_title: Aperçu WhatsApp
alias: /partners/whatsapp/
description: "Cet article fournit un aperçu du canal WhatsApp de Braze, les prérequis et des conseils pour démarrer l’intégration."
page_type: partner
search_tag: Partenaire
page_order: 0
channel:
  - WhatsApp
---

# Aperçu WhatsApp

> La messagerie [WhatsApp](https://www.whatsapp.com/) Business est une plateforme d’envoi de messages pair-à-pair populaire utilisée dans le monde entier et qui propose une messagerie basée sur les conversations pour les entreprises.	

## Conditions préalables

Acceptez les conditions suivantes avant de poursuivre avec l’intégration :

- **Politique d’abonnement :** WhatsApp exige que les entreprises demandent un abonnement des clients pour l’envoi de messages.
- **Règles de contenu WhatsApp :** WhatsApp possède plusieurs [règles de contenu](https://www.whatsapp.com/legal/commerce-policy?l=en) qui doivent être suivies.
- **Conformité :** Respectez toutes les documentations de Braze et de Meta, ainsi que toutes les [Méta-politiques](https://www.whatsapp.com/legal/?lang=en) applicables.
- **Limites de conversation de 24 heures :** Lorsqu’une entreprise envoie le message modélisé d’origine ou qu’un utilisateur envoie un message, une période de 24 heures s’ouvre au cours de laquelle les deux participants peuvent converser. 
- **Débuter une conversation :** Les utilisateurs peuvent débuter une conversation à tout moment. Une entreprise peut débuter une conversation uniquement à l’aide d’un modèle de message approuvé.
- **Limitations de compte :** Chaque groupe d’apps Braze peut détenir un compte WhatsApp Business, un groupe d’abonnement et un numéro de téléphone. De plus, chaque compte WhatsApp Business peut contenir [une seule intégration tierce](https://developers.facebook.com/docs/whatsapp/embedded-signup/faq#faq_194614375799047). 
<br><br>

| Condition| Description|
| ---| --- |
| Compte gestionnaire Meta Business | Un compte Meta Business est nécessaire pour exploiter ce canal de communication. |
| Compte WhatsApp Business | Un compte WhatsApp Business est nécessaire pour exploiter ce canal de communication. |
| Numéro de téléphone WhatsApp | Vous devez acquérir un numéro de téléphone qui correspond aux [exigences WhatsApp](https://developers.facebook.com/docs/whatsapp/phone-numbers/) pour l’utilisation du canal de communication.  | 
{: .reset-td-br-1 .reset-td-br-2}

## Intégration

### Étape 1 : Connecter WhatsApp Messenger à Braze

Dans Braze, accédez à **Technology Partners (partenaires technologiques)** puis recherchez **WhatsApp**. Sur la page partenaire WhatsApp, sélectionnez **Se connecter avec Facebook** pour débuter le processus d’intégration.

![][1]{: style="max-width:70%;"}

Il est probable que vous ayez déjà au moins un compte Meta Business existant dans votre entreprise. Si c’est le cas, sélectionnez celui que vous souhaitez utiliser pour votre compte WhatsApp Business. Les autorisations utilisateur et les vérifications commerciales pour WhatsApp seront contrôlées de manière centralisée dans votre compte Meta Business.

### Étape 2 : Paramétrage WhatsApp
Vous serez ensuite invité à interagir avec l’assistant de configuration de Braze. Lors de ce flux vous allez :
1. Créer ou sélectionner vos comptes Meta et WhatsApp Business.
2. Créer votre profil WhatsApp Business.
3. Vérifier votre numéro WhatsApp Business.<br><br>

	![][2]{: style="max-width:100%;"}

{% alert note %}
Les comptes WhatsApp Business (WABA) ne peuvent pas être partagés avec plusieurs fournisseurs de solutions d’entreprise. Vous aurez besoin d’un WABA spécifique pour chaque groupe d’apps Braze.
{% endalert %}	

Une fois le paramétrage terminé, un groupe d’abonnement dédié à WhatsApp sera créé pour vos utilisateurs.

### Étape 3 : Créer des modèles WhatsApp

Les modèles de message WhatsApp approuvés sont les seuls à pouvoir être utilisés pour démarrer une conversation avec des clients. Les modèles WhatsApp peuvent être construits dans le [gestionnaire Meta Business](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343).

1. **Accéder au [gestionnaire de modèles](https://business.facebook.com/wa/manage/message-templates)**<br>
Dans le gestionnaire Meta Business, dans **Outils de compte**, sélectionnez **Modèles de message**.
Sélectionnez ensuite **Créer des modèles**.<br><br>![][3]{: style="max-width:100%;"}<br><br>
2. **Paramètres de message**<br>
Dans l’assistant de nouveau modèle de message, sélectionnez la catégorie de votre message, renommez votre modèle et choisissez les langues que vous voulez prendre en charge. Vous pouvez en supprimer ou ajouter d’autres langues par la suite.<br><br> 
	Les catégories de modèle de message disponibles comprennent les suivantes :
	- Marketing : Envoyer des offres promotionnelles, annoncer des produits et plus encore pour accroître la connaissance et l’engagement
	- Utilitaire : Envoyer des mises à jour de compte, de commande, des alertes et plus encore pour partager des informations importantes
	- Authentification : Envoyer des codes permettant à vos clients d’accéder à leur compte<br><br> 
	![][4]{: style="max-width:100%;"}<br><br>
3. **Éditer un modèle**<br>
Il vous sera ensuite demandé de créer votre modèle de message. <br><br>Vous pouvez fournir ici un en-tête sous forme de texte ou de média, le texte du corps, un pied de page de message et des boutons. Notez que les en-têtes de vidéo et de document ne sont pas disponibles actuellement, et que les en-têtes doivent être de type texte ou image. La prévisualisation de votre message s’affichera à droite. <br><br>Même si Meta ne prend pas Liquid en charge, vous pouvez modéliser des variables qui seront ensuite remplacées par des variables Liquid dans Braze. Sélectionnez le bouton **+ Ajouter une variable** pour ce faire.<br><br>![][5]{: style="max-width:100%;"}<br><br>Une fois votre modèle terminé, cliquez **Soumettre**. 

#### Délai d’approbation du modèle

Vous pouvez vérifier le statut d’approbation de votre modèle de message sur la page **Message Template (Modèle de message)** dans le gestionnaire Meta Business ou lors de la création d’une campagne ou d’un Canvas à Braze. En outre, vous pouvez être notifié par e-mail par l’équipe WhatsApp en fonction de vos autorisations de notification. 

### Étape 4 : Créer une campagne WhatsApp

Une fois que les modèles WhatsApp sont approuvés, vous pouvez passer au tableau de bord pour construire une [campagne ou un Canvas WhatsApp]({{site.baseurl}}/user_guide/message_building_by_channel/whatsapp/create/). 

## Étapes suivantes

Après avoir terminé l’intégration, nous vous recommandons d’effectuer les deux processus Meta suivants :
- [Vérification commerciale](https://www.facebook.com/business/help/2058515294227817?id=180505742745347)
	- Vous avez peut-être déjà une vérification commerciale si vous avez utilisé un gestionnaire Meta Business existant. 
- [Compte Business officiel](https://www.facebook.com/business/help/604726921052590?ref=search_new_0)

Nous vous recommandons également de vous renseigner au sujet des [numéros de téléphone des utilisateurs]({{iste.baseurl}}/user_guide/message_building_by_channel/whatsapp/user_phone_numbers/) et d’ajouter tous les utilisateurs qui auront besoin d’un accès pour créer des [modèles de message dans votre organisation](https://www.facebook.com/business/help/2169003770027706?id=2190812977867143).


[1]: {% image_buster /assets/img/whatsapp/whatsapp1.png %} 
[2]: {% image_buster /assets/img/whatsapp/whatsapp2.gif %} 
[3]: {% image_buster /assets/img/whatsapp/whatsapp2.png %} 
[4]: {% image_buster /assets/img/whatsapp/whatsapp3.png %} 
[5]: {% image_buster /assets/img/whatsapp/whatsapp4.png %} 
[6]: {% image_buster /assets/img/whatsapp/whatsapp5.png %} 
