---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527064"
---
# <span data-ttu-id="2aaf8-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="2aaf8-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="2aaf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2aaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf8-103">Skapa en ny CommunicationService eller uppdatera en befintlig CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="2aaf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2aaf8-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2aaf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2aaf8-105">DESCRIPTION</span></span>
<span data-ttu-id="2aaf8-106">Skapa en ny CommunicationService eller uppdatera en befintlig CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="2aaf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2aaf8-107">EXAMPLES</span></span>

### <span data-ttu-id="2aaf8-108">Exempel 1: skapa en ACS-resurs</span><span class="sxs-lookup"><span data-stu-id="2aaf8-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="2aaf8-109">Skapar en ACS-resurs med de angivna parametrarna.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="2aaf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2aaf8-110">PARAMETERS</span></span>

### <span data-ttu-id="2aaf8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aaf8-111">-AsJob</span></span>
<span data-ttu-id="2aaf8-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2aaf8-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="2aaf8-113">-DataLocation</span></span>
<span data-ttu-id="2aaf8-114">Platsen där kommunikations tjänsten lagrar sina data på rest.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf8-115">-DefaultProfile</span></span>
<span data-ttu-id="2aaf8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aaf8-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="2aaf8-117">-Location</span></span>
<span data-ttu-id="2aaf8-118">Den Azure-plats där CommunicationService körs.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2aaf8-119">-Name</span></span>
<span data-ttu-id="2aaf8-120">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2aaf8-121">-NoWait</span></span>
<span data-ttu-id="2aaf8-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2aaf8-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf8-123">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf8-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2aaf8-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2aaf8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2aaf8-126">-SubscriptionId</span></span>
<span data-ttu-id="2aaf8-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2aaf8-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2aaf8-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2aaf8-129">-Tag</span></span>
<span data-ttu-id="2aaf8-130">Taggar för tjänsten som är en lista över de värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf8-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2aaf8-131">-Confirm</span></span>
<span data-ttu-id="2aaf8-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aaf8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aaf8-133">-WhatIf</span></span>
<span data-ttu-id="2aaf8-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aaf8-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aaf8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf8-136">CommonParameters</span></span>
<span data-ttu-id="2aaf8-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaf8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf8-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aaf8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf8-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2aaf8-139">INPUTS</span></span>

## <span data-ttu-id="2aaf8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2aaf8-140">OUTPUTS</span></span>

### <span data-ttu-id="2aaf8-141">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="2aaf8-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="2aaf8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2aaf8-142">NOTES</span></span>

<span data-ttu-id="2aaf8-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2aaf8-143">ALIASES</span></span>

## <span data-ttu-id="2aaf8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2aaf8-144">RELATED LINKS</span></span>

