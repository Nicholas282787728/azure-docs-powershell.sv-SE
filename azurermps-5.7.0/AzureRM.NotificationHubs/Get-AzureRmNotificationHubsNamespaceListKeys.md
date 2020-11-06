---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespacelistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 2fb9eeb3b5d6bcc3a2183bc652b74caa370e4d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577115"
---
# <span data-ttu-id="6ecf5-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="6ecf5-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="6ecf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ecf5-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecf5-103">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ecf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ecf5-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ecf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ecf5-105">DESCRIPTION</span></span>
<span data-ttu-id="6ecf5-106">Cmdleten **Get-AzureRmNotificationHubsNamespaceListKeys** returnerar de primära och sekundära anslutnings strängarna för en auktoriseringsregel för en delad Access-signatur som tilldelats ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="6ecf5-107">Auktoriseringsregler hanterar användar rättigheter till ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="6ecf5-108">Varje regel innehåller en primär och en sekundär anslutnings sträng.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="6ecf5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ecf5-109">EXAMPLES</span></span>

### <span data-ttu-id="6ecf5-110">Exempel 1: Hämta primära och sekundära anslutnings strängar för en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="6ecf5-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6ecf5-111">Det här kommandot returnerar de primära och sekundära anslutnings strängarna för auktoriseringsregeln som heter ListenRule tilldelade till ContosoNamespace namn området.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="6ecf5-112">När du kör det här kommandot måste du ange namnet på den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="6ecf5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ecf5-113">PARAMETERS</span></span>

### <span data-ttu-id="6ecf5-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6ecf5-114">-AuthorizationRule</span></span>
<span data-ttu-id="6ecf5-115">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="6ecf5-116">Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-116">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ecf5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecf5-117">-DefaultProfile</span></span>
<span data-ttu-id="6ecf5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6ecf5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecf5-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6ecf5-119">-Namespace</span></span>
<span data-ttu-id="6ecf5-120">Anger namn området som innehåller de anslutnings strängar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ecf5-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ecf5-121">-ResourceGroup</span></span>
<span data-ttu-id="6ecf5-122">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-122">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="6ecf5-123">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ecf5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecf5-124">CommonParameters</span></span>
<span data-ttu-id="6ecf5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecf5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ecf5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecf5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ecf5-127">INPUTS</span></span>

### <span data-ttu-id="6ecf5-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="6ecf5-128">None</span></span>
<span data-ttu-id="6ecf5-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6ecf5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ecf5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ecf5-130">OUTPUTS</span></span>

### <span data-ttu-id="6ecf5-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6ecf5-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6ecf5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ecf5-132">NOTES</span></span>

## <span data-ttu-id="6ecf5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ecf5-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ecf5-134">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6ecf5-134">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="6ecf5-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6ecf5-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


