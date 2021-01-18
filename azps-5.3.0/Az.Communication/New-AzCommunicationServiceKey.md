---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524574"
---
# <span data-ttu-id="b78ca-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="b78ca-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="b78ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b78ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b78ca-103">Återskapa CommunicationService-åtkomst nyckeln.</span><span class="sxs-lookup"><span data-stu-id="b78ca-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="b78ca-104">PrimaryKey och SecondaryKey kan inte återskapas samtidigt.</span><span class="sxs-lookup"><span data-stu-id="b78ca-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="b78ca-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b78ca-105">SYNTAX</span></span>

### <span data-ttu-id="b78ca-106">RegenerateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="b78ca-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b78ca-107">Återskapa</span><span class="sxs-lookup"><span data-stu-id="b78ca-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b78ca-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b78ca-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b78ca-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b78ca-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b78ca-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b78ca-110">DESCRIPTION</span></span>
<span data-ttu-id="b78ca-111">Återskapa CommunicationService-åtkomst nyckeln.</span><span class="sxs-lookup"><span data-stu-id="b78ca-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="b78ca-112">PrimaryKey och SecondaryKey kan inte återskapas samtidigt.</span><span class="sxs-lookup"><span data-stu-id="b78ca-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="b78ca-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b78ca-113">EXAMPLES</span></span>

### <span data-ttu-id="b78ca-114">Exempel 1: återskapa primär nyckeln med en IRegenerateKeyParameters-hash</span><span class="sxs-lookup"><span data-stu-id="b78ca-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="b78ca-115">Upphäver den föregående primär nyckeln, återskapa en ny och returnera den.</span><span class="sxs-lookup"><span data-stu-id="b78ca-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="b78ca-116">Exempel 2: återskapa den sekundära nyckeln med en värdetyp</span><span class="sxs-lookup"><span data-stu-id="b78ca-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="b78ca-117">Upphäver den föregående sekundära nyckeln, återskapa en ny och returnera den.</span><span class="sxs-lookup"><span data-stu-id="b78ca-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="b78ca-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b78ca-118">PARAMETERS</span></span>

### <span data-ttu-id="b78ca-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="b78ca-119">-CommunicationServiceName</span></span>
<span data-ttu-id="b78ca-120">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78ca-121">-DefaultProfile</span></span>
<span data-ttu-id="b78ca-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b78ca-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78ca-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b78ca-123">-InputObject</span></span>
<span data-ttu-id="b78ca-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b78ca-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-125">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="b78ca-125">-KeyType</span></span>
<span data-ttu-id="b78ca-126">Vilken typ du vill återskapa.</span><span class="sxs-lookup"><span data-stu-id="b78ca-126">The keyType to regenerate.</span></span>
<span data-ttu-id="b78ca-127">Måste vara antingen "Primary" eller "Secondary" (Skift läges okänsligt).</span><span class="sxs-lookup"><span data-stu-id="b78ca-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b78ca-128">-Parameter</span></span>
<span data-ttu-id="b78ca-129">Parametrar beskriver begäran om att skapa åtkomst nycklar att konstruera, se avsnittet anteckningar för PARAMETER egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b78ca-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b78ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="b78ca-131">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b78ca-132">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b78ca-133">-SubscriptionId</span></span>
<span data-ttu-id="b78ca-134">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b78ca-135">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b78ca-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78ca-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b78ca-136">-Confirm</span></span>
<span data-ttu-id="b78ca-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b78ca-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b78ca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b78ca-138">-WhatIf</span></span>
<span data-ttu-id="b78ca-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b78ca-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b78ca-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b78ca-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b78ca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78ca-141">CommonParameters</span></span>
<span data-ttu-id="b78ca-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b78ca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78ca-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b78ca-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78ca-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b78ca-144">INPUTS</span></span>

### <span data-ttu-id="b78ca-145">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="b78ca-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="b78ca-146">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="b78ca-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="b78ca-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b78ca-147">OUTPUTS</span></span>

### <span data-ttu-id="b78ca-148">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b78ca-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="b78ca-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b78ca-149">NOTES</span></span>

<span data-ttu-id="b78ca-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b78ca-150">ALIASES</span></span>

<span data-ttu-id="b78ca-151">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b78ca-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b78ca-152">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b78ca-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b78ca-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b78ca-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b78ca-154">INPUTOBJECT <ICommunicationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b78ca-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b78ca-155">`[CommunicationServiceName <String>]`: Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="b78ca-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b78ca-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b78ca-157">`[Location <String>]`: Azure-regionen</span><span class="sxs-lookup"><span data-stu-id="b78ca-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="b78ca-158">`[OperationId <String>]`: ID för pågående asynkron åtgärd</span><span class="sxs-lookup"><span data-stu-id="b78ca-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="b78ca-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b78ca-160">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b78ca-161">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b78ca-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b78ca-162">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b78ca-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b78ca-163">PARAMETER <IRegenerateKeyParameters> : Här beskrivs begäran om att återskapa åtkomst nycklar</span><span class="sxs-lookup"><span data-stu-id="b78ca-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="b78ca-164">`[KeyType <KeyType?>]`: Den typ du vill återskapa.</span><span class="sxs-lookup"><span data-stu-id="b78ca-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="b78ca-165">Måste vara antingen "Primary" eller "Secondary" (Skift läges okänsligt).</span><span class="sxs-lookup"><span data-stu-id="b78ca-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="b78ca-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b78ca-166">RELATED LINKS</span></span>

