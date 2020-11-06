---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 539a0471ae27adc80b67360fc47955fdb4b50bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573934"
---
# <span data-ttu-id="26cc2-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="26cc2-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="26cc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="26cc2-103">Push Mobility Service Agent-uppdateringar till skyddade datorer.</span><span class="sxs-lookup"><span data-stu-id="26cc2-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26cc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26cc2-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26cc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="26cc2-106">Cmdleten **Update-AzureRmRecoveryServicesAsrMobilityService** försöker skicka push Mobility Service Agent-uppdateringar till skyddade datorer (om det finns en tillgänglig uppdatering.)</span><span class="sxs-lookup"><span data-stu-id="26cc2-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="26cc2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="26cc2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26cc2-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="26cc2-109">Jobb för att spåra uppdatering av skyddat objekt för Moblility-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26cc2-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="26cc2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26cc2-110">PARAMETERS</span></span>

### <span data-ttu-id="26cc2-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="26cc2-111">-Account</span></span>
<span data-ttu-id="26cc2-112">ID för kör som-konto som ska användas för att skicka uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="26cc2-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="26cc2-113">Måste finnas i listan med kör som-konton i ASR-infrastrukturen som motsvarar den dator som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="26cc2-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cc2-114">-DefaultProfile</span></span>
<span data-ttu-id="26cc2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26cc2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cc2-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26cc2-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26cc2-117">Det skyddade objektet för replikering av Azure Site Recovery-objekt uppdateras.</span><span class="sxs-lookup"><span data-stu-id="26cc2-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26cc2-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26cc2-118">-Confirm</span></span>
<span data-ttu-id="26cc2-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26cc2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26cc2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26cc2-120">-WhatIf</span></span>
<span data-ttu-id="26cc2-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26cc2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26cc2-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26cc2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26cc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cc2-123">CommonParameters</span></span>
<span data-ttu-id="26cc2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26cc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cc2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26cc2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26cc2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26cc2-126">INPUTS</span></span>

### <span data-ttu-id="26cc2-127">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26cc2-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="26cc2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26cc2-128">OUTPUTS</span></span>

### <span data-ttu-id="26cc2-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="26cc2-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26cc2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26cc2-130">NOTES</span></span>

## <span data-ttu-id="26cc2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26cc2-131">RELATED LINKS</span></span>
