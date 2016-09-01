<properties
   pageTitle="Aan de slag met Azure AD Privileged Identity Management | Microsoft Azure"
   description="Informatie over het beheren van bevoegde identiteiten met de Azure Active Directory Privileged Identity Management-toepassing in Azure-portal."
   services="active-directory"
   documentationCenter=""
   authors="kgremban"
   manager="femila"
   editor=""/>

<tags
   ms.service="active-directory"
   ms.devlang="na"
   ms.topic="get-started-article"
   ms.tgt_pltfrm="na"
   ms.workload="identity"
   ms.date="06/29/2016"
   ms.author="kgremban"/>

# Aan de slag met Azure AD Privileged Identity Management


Met Azure Active Directory (AD) Privileged Identity Management kunt u bevoegde identiteiten en de toegang tot bronnen in Azure AD en andere Microsoft Online Services, zoals Office 365 of Microsoft Intune, beheren en controleren.  

In dit artikel leest u hoe u de PIM-app van Azure AD toevoegt aan uw Azure-portaldashboard.

## De Privileged Identity Management-toepassing toevoegen

Voordat u Azure AD Privileged Identity Management gebruikt, moet u de toepassing toevoegen aan uw Azure-portaldashboard.

1. Meld u aan bij de [Azure-portal](https://portal.azure.com/) als globale beheerder van uw directory.
2. Als uw organisatie meerdere directory's heeft, klikt u op uw gebruikersnaam rechtsboven in de Azure-portal en selecteert u de directory waarin u PIM gebruikt.
3. Selecteer **Nieuw** > **Beveiliging en identiteit** > **Azure AD Privileged Identity Management**.

    ![PIM inschakelen in de portal][1]

4. Schakel **Vastmaken aan dashboard** in en klik op de knop **Maken**. De Privileged Identity Management-toepassing wordt geopend.


Als u de eerste persoon bent die Azure AD Privileged Identity Management in uw directory gebruikt, wordt u via de [wizard Beveiliging](active-directory-privileged-identity-management-security-wizard.md) stapsgewijs begeleid bij de eerste toewijzing. Hierna wordt u automatisch de eerste **beveiligingsbeheerder** en **beheerder met bevoorrechte rol** van de directory. Alleen een beheerder met bevoorrechte rol heeft toegang tot deze toepassing om de toegang voor andere beheerders te beheren.  

Als u een of meer rollen toegewezen hebt gekregen, beschikt u over de optie **Mijn rollen activeren**. Als u een beheerder met bevoorrechte rol bent, ziet u ook een optie **Bevoorrechte rollen beheren**.  


<!--Every topic should have next steps and links to the next logical set of content to keep the customer engaged-->
## Volgende stappen

Het [overzicht van Azure AD Privileged Identity Management](active-directory-privileged-identity-management-configure.md) bevat meer informatie over het beheren van beheerderstoegang in uw organisatie.

[AZURE.INCLUDE [active-directory-privileged-identity-management-toc](../../includes/active-directory-privileged-identity-management-toc.md)]

<!--Image references-->

[1]: ./media/active-directory-privileged-identity-management-configure/PIM_EnablePim.png



<!--HONumber=ago16_HO4-->


