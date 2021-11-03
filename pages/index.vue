<template>
<div>
  <section class="mx-28 mt-24" >
    <FaqItem 
      v-for="(item,index) in data" 
      :key="item.title" 
      v-bind:index="index"
      v-bind:title="item.title" 
      v-bind:subTitle="item.subtitle" 
      v-bind:content="item.content"
    />
  </section>

  <section class="mx-28 mt-24 md:my-24">
    <h3 class="text-xl md:text-4xl font-semibold mb-8">Vous n’avez pas trouvé de réponse à votre question ? Contactez-nous !</h3>
    <div class="flex flex-col md:flex-row md:flex-wrap">
      <div class="flex  mb-4 md:mr-24 last:mr-0"><div class="mr-6 my-auto"><a href="tel:02 37 64 84 40" class="md:hidden block"><img src="https://admin.shoppingauto.fr/storage/uploads/2020/12/15/5fd88680e42195d7fae39ec200PICTO_Hotline.svg" class="w-16"></a> <button class="hidden md:block"><img src="https://admin.shoppingauto.fr/storage/uploads/2020/12/15/5fd88680e42195d7fae39ec200PICTO_Hotline.svg" class="w-16"></button></div> <div class="my-auto flex-1"><p class="text-base md:text-xl font-semibold">
          Hotline téléphonique
        </p> 
      <div class="text-sm"><p>Du lundi au samedi de 9h00 à 19h00 au <a href="tel:0237648440">02 37 64 84 40</a>.</p></div></div></div><div class="flex mb-4 md:mr-24 last:mr-0"><img src="https://admin.shoppingauto.fr/storage/uploads/2020/12/15/5fd886839aec65d7fae3a008b3PICTO_Chat.svg" class="w-16 my-auto mr-6"> <div class="my-auto flex-1"><p class="text-base md:text-xl font-semibold">
          Chat en ligne
        </p> <div class="text-sm">7 jours sur 7, de 6h à minuit</div></div></div>
    </div>
  </section>
</div>
</template>

<script>

import FaqItem from '~/components/FaqItem';

export default {

  components: { FaqItem },

  data(){
    const subtitle = "La réponse de shoppingauto.fr :"
    const data = [
      {title:"shoppingauto.fr, comment ça marche ?", subtitle, content:"Acheter une auto n'aura jamais été aussi facile. Cherchez, comparez et réservez ! Dès réception de votre réservation, on se charge de finaliser votre commande à vos côtés et à 100% en digital ! 😊"},
      {title:"J'aimerai avoir des infos complémentaires sur un véhicule ?", subtitle, content:"Une question sur la finition ?  Les options ? Une trace d'usure ? Nos conseillers shoppingauto.fr vous répondent directement sur notre chat ! 😎"},
      {title:"Comment savoir combien coutera ma livraison ?", subtitle, content:'Rien de plus simple : Une fois votre véhicule choisie, appuyez sur le bouton "je shop" et une étape plus tard on vous demandera dans quel département vous souhaitait être livré et on vous indiquera le tarif ! 🚀'},
      {title:"Comment réserver le véhicule ?", subtitle, content:"Afin de bloquer la voiture de vos rêves, nous vous invitons à réserver le véhicule en ligne en versant un acompte de 250€, un bon de réservation vous sera transmis automatiquement par mail. "},
      {title:"Comment payer le solde du véhicule ?", subtitle, content:"Le montant de l'acompte sera enlevé du montant global et notre service administratif se chargera de vous envoyer la facture, le bon de commande et notre RIB. Pour le paiement du solde, un virement sera exigé en amont de la livraison et dès reception des fonds, la livraison pourra être effectuée."},
      {title:"Que faire si le véhicule ne me convient pas ?", subtitle, content:"Pas de panique ! Vous êtes protégé avec notre garantie satisfait ou remboursé."}
    ]
    return {data};
  }

};

</script>