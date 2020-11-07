---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: c099f3d8419e7298af1a262f824304d50685a420
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747627"
---
# <span data-ttu-id="10c46-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="10c46-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="10c46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10c46-102">SYNOPSIS</span></span>
<span data-ttu-id="10c46-103">Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="10c46-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="10c46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10c46-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10c46-105">DESCRIPTION</span></span>
<span data-ttu-id="10c46-106">Cmdleten **Get-AzNotificationHubsNamespaceListKey** returnerar de primära och sekundära anslutnings strängarna för en auktoriseringsregel för en delad Access-signatur som tilldelats ett namn område i en aviserings hubb.</span><span class="sxs-lookup"><span data-stu-id="10c46-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="10c46-107">Auktoriseringsregler hanterar användar rättigheter till ett namn område för aviseringar.</span><span class="sxs-lookup"><span data-stu-id="10c46-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="10c46-108">Varje regel innehåller en primär och en sekundär anslutnings sträng.</span><span class="sxs-lookup"><span data-stu-id="10c46-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="10c46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10c46-109">EXAMPLES</span></span>

### <span data-ttu-id="10c46-110">Exempel 1: Hämta primära och sekundära anslutnings strängar för en auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="10c46-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="10c46-111">Det här kommandot returnerar de primära och sekundära anslutnings strängarna för auktoriseringsregeln som heter ListenRule tilldelade till ContosoNamespace namn området.</span><span class="sxs-lookup"><span data-stu-id="10c46-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="10c46-112">När du kör det här kommandot måste du ange namnet på den resurs grupp som namn området är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="10c46-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="10c46-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10c46-113">PARAMETERS</span></span>

### <span data-ttu-id="10c46-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10c46-114">-AuthorizationRule</span></span>
<span data-ttu-id="10c46-115">Anger namnet på en SAS-autentiseringsprocess.</span><span class="sxs-lookup"><span data-stu-id="10c46-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="10c46-116">Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.</span><span class="sxs-lookup"><span data-stu-id="10c46-116">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c46-117">-DefaultProfile</span></span>
<span data-ttu-id="10c46-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="10c46-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c46-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="10c46-119">-Namespace</span></span>
<span data-ttu-id="10c46-120">Anger namn området som innehåller de anslutnings strängar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="10c46-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c46-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10c46-121">-ResourceGroup</span></span>
<span data-ttu-id="10c46-122">Anger den resurs grupp som namn området tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="10c46-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="10c46-123">Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.</span><span class="sxs-lookup"><span data-stu-id="10c46-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c46-124">CommonParameters</span></span>
<span data-ttu-id="10c46-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c46-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c46-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10c46-127">INPUTS</span></span>

### <span data-ttu-id="10c46-128">System. String</span><span class="sxs-lookup"><span data-stu-id="10c46-128">System.String</span></span>

## <span data-ttu-id="10c46-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10c46-129">OUTPUTS</span></span>

### <span data-ttu-id="10c46-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="10c46-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="10c46-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10c46-131">NOTES</span></span>

## <span data-ttu-id="10c46-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10c46-132">RELATED LINKS</span></span>

[<span data-ttu-id="10c46-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="10c46-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="10c46-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="10c46-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


