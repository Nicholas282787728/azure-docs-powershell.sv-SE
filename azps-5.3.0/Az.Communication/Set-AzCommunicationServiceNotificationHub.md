---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524573"
---
# <span data-ttu-id="33dfa-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="33dfa-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="33dfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="33dfa-103">Länkar en Azure Notification-hubb till den här kommunikations tjänsten.</span><span class="sxs-lookup"><span data-stu-id="33dfa-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="33dfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33dfa-104">SYNTAX</span></span>

### <span data-ttu-id="33dfa-105">LinkExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="33dfa-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="33dfa-106">Länknamn</span><span class="sxs-lookup"><span data-stu-id="33dfa-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33dfa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="33dfa-108">Länkar en Azure Notification-hubb till den här kommunikations tjänsten.</span><span class="sxs-lookup"><span data-stu-id="33dfa-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="33dfa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33dfa-109">EXAMPLES</span></span>

### <span data-ttu-id="33dfa-110">Exempel 1: Tillhandahåll interaktivt med information om meddelandets hubb</span><span class="sxs-lookup"><span data-stu-id="33dfa-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="33dfa-111">Med en länkad meddelande hubb kan en ACS-resurs skicka aviseringar för vissa händelser.</span><span class="sxs-lookup"><span data-stu-id="33dfa-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="33dfa-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33dfa-112">PARAMETERS</span></span>

### <span data-ttu-id="33dfa-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="33dfa-113">-CommunicationServiceName</span></span>
<span data-ttu-id="33dfa-114">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="33dfa-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="33dfa-115">-ConnectionString</span></span>
<span data-ttu-id="33dfa-116">Anslutnings sträng för meddelande navet</span><span class="sxs-lookup"><span data-stu-id="33dfa-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dfa-117">-DefaultProfile</span></span>
<span data-ttu-id="33dfa-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33dfa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="33dfa-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="33dfa-120">Beskrivning av ett Azure Notification-nav som länkar till kommunikations tjänsten för att skapa, se avsnittet anteckningar för LINKNOTIFICATIONHUBPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="33dfa-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="33dfa-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="33dfa-122">Resurs-ID för meddelande navet</span><span class="sxs-lookup"><span data-stu-id="33dfa-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dfa-123">-ResourceGroupName</span></span>
<span data-ttu-id="33dfa-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="33dfa-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="33dfa-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="33dfa-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33dfa-126">-SubscriptionId</span></span>
<span data-ttu-id="33dfa-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33dfa-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="33dfa-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="33dfa-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33dfa-129">-Confirm</span></span>
<span data-ttu-id="33dfa-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33dfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33dfa-131">-WhatIf</span></span>
<span data-ttu-id="33dfa-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33dfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33dfa-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33dfa-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33dfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dfa-134">CommonParameters</span></span>
<span data-ttu-id="33dfa-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dfa-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33dfa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dfa-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33dfa-137">INPUTS</span></span>

### <span data-ttu-id="33dfa-138">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="33dfa-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="33dfa-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33dfa-139">OUTPUTS</span></span>

### <span data-ttu-id="33dfa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="33dfa-140">System.String</span></span>

## <span data-ttu-id="33dfa-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33dfa-141">NOTES</span></span>

<span data-ttu-id="33dfa-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33dfa-142">ALIASES</span></span>

<span data-ttu-id="33dfa-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="33dfa-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33dfa-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="33dfa-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33dfa-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33dfa-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33dfa-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters> : Beskrivning av ett Azure Notification Hub som länkar till kommunikations tjänsten</span><span class="sxs-lookup"><span data-stu-id="33dfa-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="33dfa-147">`ConnectionString <String>`: Anslutnings sträng för meddelande navet</span><span class="sxs-lookup"><span data-stu-id="33dfa-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="33dfa-148">`ResourceId <String>`: Meddelande navets resurs-ID</span><span class="sxs-lookup"><span data-stu-id="33dfa-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="33dfa-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33dfa-149">RELATED LINKS</span></span>

