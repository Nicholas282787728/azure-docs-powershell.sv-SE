---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099944"
---
# <span data-ttu-id="7c730-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7c730-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="7c730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c730-102">SYNOPSIS</span></span>
<span data-ttu-id="7c730-103">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="7c730-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="7c730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c730-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c730-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c730-105">DESCRIPTION</span></span>
<span data-ttu-id="7c730-106">Avbryta ett migreringsjobb.</span><span class="sxs-lookup"><span data-stu-id="7c730-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="7c730-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c730-107">EXAMPLES</span></span>

### <span data-ttu-id="7c730-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="7c730-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="7c730-109">Avbryta ett migreringsarkiv för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="7c730-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="7c730-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c730-110">PARAMETERS</span></span>

### <span data-ttu-id="7c730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c730-111">-DefaultProfile</span></span>
<span data-ttu-id="7c730-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c730-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c730-113">-Location</span></span>
<span data-ttu-id="7c730-114">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="7c730-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c730-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c730-115">-Name</span></span>
<span data-ttu-id="7c730-116">GUID-namnet för migreringen.</span><span class="sxs-lookup"><span data-stu-id="7c730-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c730-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c730-117">-SubscriptionId</span></span>
<span data-ttu-id="7c730-118">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7c730-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c730-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7c730-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7c730-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c730-120">-Confirm</span></span>
<span data-ttu-id="7c730-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c730-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c730-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c730-122">-WhatIf</span></span>
<span data-ttu-id="7c730-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c730-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c730-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c730-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c730-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c730-125">CommonParameters</span></span>
<span data-ttu-id="7c730-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c730-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c730-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c730-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c730-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c730-128">INPUTS</span></span>

## <span data-ttu-id="7c730-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c730-129">OUTPUTS</span></span>

### <span data-ttu-id="7c730-130">Microsoft. Azure. PowerShell. cmdletar. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="7c730-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="7c730-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c730-131">NOTES</span></span>

## <span data-ttu-id="7c730-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c730-132">RELATED LINKS</span></span>
