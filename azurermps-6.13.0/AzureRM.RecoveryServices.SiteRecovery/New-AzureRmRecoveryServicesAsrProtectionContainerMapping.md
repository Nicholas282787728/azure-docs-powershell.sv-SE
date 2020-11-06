---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 35e338d5e6fd9dccbee1a099bc4dabf234cd8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572660"
---
# <span data-ttu-id="4e224-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4e224-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="4e224-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e224-102">SYNOPSIS</span></span>
<span data-ttu-id="4e224-103">Skapar en mappning av en behållare för Azure Site Recovery-skydd genom att associera den angivna replikeringsprincipen till den angivna tjänsten för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="4e224-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e224-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e224-104">SYNTAX</span></span>

### <span data-ttu-id="4e224-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="4e224-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e224-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="4e224-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e224-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e224-107">DESCRIPTION</span></span>
<span data-ttu-id="4e224-108">Cmdleten **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** skapar en mappning för Azure Site Recovery-skydd genom att associera den angivna replikeringsprincipen till den angivna skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="4e224-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="4e224-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e224-109">EXAMPLES</span></span>

### <span data-ttu-id="4e224-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e224-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="4e224-111">Startar skapandet av mappning av skydds behållare med angivna parametrar och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4e224-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="4e224-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4e224-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="4e224-113">Startar skapandet av mappning av skydds behållare med angivna parametrar och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4e224-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4e224-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e224-114">PARAMETERS</span></span>

### <span data-ttu-id="4e224-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e224-115">-DefaultProfile</span></span>
<span data-ttu-id="4e224-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e224-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4e224-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e224-117">-Name</span></span>
<span data-ttu-id="4e224-118">Anger namnet på skydds behållar mappningen.</span><span class="sxs-lookup"><span data-stu-id="4e224-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="4e224-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="4e224-119">-Policy</span></span>
<span data-ttu-id="4e224-120">Anger ASR-principobjektet för den replikeringsprincip som ska användas i mappningen.</span><span class="sxs-lookup"><span data-stu-id="4e224-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e224-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4e224-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="4e224-122">Anger att objektet ASR Protection container för den primära skydds behållaren ska användas i mappningen.</span><span class="sxs-lookup"><span data-stu-id="4e224-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e224-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4e224-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="4e224-124">Anger att objektet ASR Protection container för den återställnings skydds behållare som ska användas i mappningen (används om du replikerar till en återställnings plats som inte är Azure.)</span><span class="sxs-lookup"><span data-stu-id="4e224-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e224-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e224-125">-Confirm</span></span>
<span data-ttu-id="4e224-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e224-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e224-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e224-127">-WhatIf</span></span>
<span data-ttu-id="4e224-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e224-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e224-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e224-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e224-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e224-130">CommonParameters</span></span>
<span data-ttu-id="4e224-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e224-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e224-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e224-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e224-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e224-133">INPUTS</span></span>

### <span data-ttu-id="4e224-134">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="4e224-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="4e224-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e224-135">OUTPUTS</span></span>

### <span data-ttu-id="4e224-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4e224-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4e224-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e224-137">NOTES</span></span>

## <span data-ttu-id="4e224-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e224-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e224-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4e224-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="4e224-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4e224-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
