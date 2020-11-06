---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582948"
---
# <span data-ttu-id="cbbbf-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="cbbbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbbf-103">Aktiverar replikering för en skyddad artikel genom att skapa ett skyddat objekt</span><span class="sxs-lookup"><span data-stu-id="cbbbf-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbbbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbbbf-104">SYNTAX</span></span>

### <span data-ttu-id="cbbbf-105">Avaktiverare (standard)</span><span class="sxs-lookup"><span data-stu-id="cbbbf-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbbf-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cbbbf-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbbf-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cbbbf-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbbf-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="cbbbf-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbbbf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbbbf-109">DESCRIPTION</span></span>
<span data-ttu-id="cbbbf-110">Cmdleten **New-AzureRmSiteRecoveryReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="cbbbf-111">Använd denna cmdlet för att aktivera replikering för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="cbbbf-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbbbf-112">EXAMPLES</span></span>

## <span data-ttu-id="cbbbf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbbbf-113">PARAMETERS</span></span>

### <span data-ttu-id="cbbbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbbf-114">-DefaultProfile</span></span>
<span data-ttu-id="cbbbf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbbbf-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbbbf-116">-Name</span></span>
<span data-ttu-id="cbbbf-117">Anger namnet på det skyddade objektet för replikering av Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-118">-OS</span><span class="sxs-lookup"><span data-stu-id="cbbbf-118">-OS</span></span>
<span data-ttu-id="cbbbf-119">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-119">Specifies the operating system family.</span></span>
<span data-ttu-id="cbbbf-120">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="cbbbf-121">-OSDiskName</span></span>
<span data-ttu-id="cbbbf-122">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-123">-ProtectableItem</span></span>
<span data-ttu-id="cbbbf-124">Anger det skydd bara objektet för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cbbbf-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="cbbbf-126">Anger det kart objekt för Azure Site Recovery-objektet som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbbbf-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="cbbbf-128">Anger ID för det Azure Storage-konto som denna cmdlet replikerar till.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cbbbf-129">-WaitForCompletion</span></span>
<span data-ttu-id="cbbbf-130">Anger att cmdleten väntar på slut för ande.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-130">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbbbf-131">-Confirm</span></span>
<span data-ttu-id="cbbbf-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbbbf-133">-WhatIf</span></span>
<span data-ttu-id="cbbbf-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cbbbf-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbbf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbbf-136">CommonParameters</span></span>
<span data-ttu-id="cbbbf-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbbf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbbf-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbbbf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbbf-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbbbf-139">INPUTS</span></span>

### <span data-ttu-id="cbbbf-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-140">ASRProtectableItem</span></span>
<span data-ttu-id="cbbbf-141">Parametern ' ProtectableItem ' godkänner värdet av typen ' ASRProtectableItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cbbbf-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="cbbbf-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbbbf-142">OUTPUTS</span></span>

### <span data-ttu-id="cbbbf-143">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cbbbf-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cbbbf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbbbf-144">NOTES</span></span>

## <span data-ttu-id="cbbbf-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbbbf-145">RELATED LINKS</span></span>

[<span data-ttu-id="cbbbf-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="cbbbf-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="cbbbf-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbbf-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
