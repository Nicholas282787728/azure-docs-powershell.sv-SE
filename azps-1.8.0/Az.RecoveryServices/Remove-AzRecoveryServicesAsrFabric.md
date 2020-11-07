---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747370"
---
# <span data-ttu-id="360f2-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="360f2-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="360f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="360f2-102">SYNOPSIS</span></span>
<span data-ttu-id="360f2-103">Tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="360f2-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="360f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="360f2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="360f2-105">DESCRIPTION</span></span>
<span data-ttu-id="360f2-106">Cmdleten **Remove-AzRecoveryServicesAsrFabric** tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="360f2-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="360f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="360f2-107">EXAMPLES</span></span>

### <span data-ttu-id="360f2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="360f2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="360f2-109">Börjar ta bort angiven Fabric och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="360f2-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="360f2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="360f2-110">PARAMETERS</span></span>

### <span data-ttu-id="360f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360f2-111">-DefaultProfile</span></span>
<span data-ttu-id="360f2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="360f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="360f2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="360f2-113">-Force</span></span>
<span data-ttu-id="360f2-114">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="360f2-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="360f2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="360f2-115">-InputObject</span></span>
<span data-ttu-id="360f2-116">Indatavärdet till cmdleten: det ASR Fabric-objekt som motsvarar infrastruktur resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="360f2-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="360f2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="360f2-117">-Confirm</span></span>
<span data-ttu-id="360f2-118">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="360f2-118">Specify if confirmation is required.</span></span> <span data-ttu-id="360f2-119">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="360f2-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="360f2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360f2-120">-WhatIf</span></span>
<span data-ttu-id="360f2-121">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="360f2-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="360f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360f2-122">CommonParameters</span></span>
<span data-ttu-id="360f2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360f2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360f2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="360f2-125">INPUTS</span></span>

### <span data-ttu-id="360f2-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="360f2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="360f2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="360f2-127">OUTPUTS</span></span>

### <span data-ttu-id="360f2-128">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="360f2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="360f2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="360f2-129">NOTES</span></span>

## <span data-ttu-id="360f2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="360f2-130">RELATED LINKS</span></span>

[<span data-ttu-id="360f2-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="360f2-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="360f2-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="360f2-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)