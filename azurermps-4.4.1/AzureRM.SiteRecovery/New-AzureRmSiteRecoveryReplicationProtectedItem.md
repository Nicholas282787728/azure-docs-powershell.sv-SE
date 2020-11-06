---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574513"
---
# <span data-ttu-id="52d9b-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="52d9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="52d9b-103">Aktiverar replikering för en skyddad artikel genom att skapa ett skyddat objekt</span><span class="sxs-lookup"><span data-stu-id="52d9b-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52d9b-104">SYNTAX</span></span>

### <span data-ttu-id="52d9b-105">Avaktiverare (standard)</span><span class="sxs-lookup"><span data-stu-id="52d9b-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d9b-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="52d9b-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d9b-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="52d9b-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d9b-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="52d9b-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d9b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52d9b-109">DESCRIPTION</span></span>
<span data-ttu-id="52d9b-110">Cmdleten **New-AzureRmSiteRecoveryReplicationProtectedItem** skapar ett nytt replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="52d9b-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="52d9b-111">Använd denna cmdlet för att aktivera replikering för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="52d9b-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="52d9b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52d9b-112">EXAMPLES</span></span>

## <span data-ttu-id="52d9b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52d9b-113">PARAMETERS</span></span>

### <span data-ttu-id="52d9b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="52d9b-114">-Name</span></span>
<span data-ttu-id="52d9b-115">Anger namnet på det skyddade objektet för replikering av Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="52d9b-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-116">-OS</span><span class="sxs-lookup"><span data-stu-id="52d9b-116">-OS</span></span>
<span data-ttu-id="52d9b-117">Anger operativ system familjen.</span><span class="sxs-lookup"><span data-stu-id="52d9b-117">Specifies the operating system family.</span></span>
<span data-ttu-id="52d9b-118">De acceptabla värdena för denna parameter är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="52d9b-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="52d9b-119">-OSDiskName</span></span>
<span data-ttu-id="52d9b-120">Anger namnet på operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="52d9b-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-121">-ProtectableItem</span></span>
<span data-ttu-id="52d9b-122">Anger det skydd bara objektet för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="52d9b-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="52d9b-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="52d9b-124">Anger det kart objekt för Azure Site Recovery-objektet som ska användas för replikering.</span><span class="sxs-lookup"><span data-stu-id="52d9b-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="52d9b-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="52d9b-126">Anger ID för det Azure Storage-konto som denna cmdlet replikerar till.</span><span class="sxs-lookup"><span data-stu-id="52d9b-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="52d9b-127">-WaitForCompletion</span></span>
<span data-ttu-id="52d9b-128">Anger att cmdleten väntar på slut för ande.</span><span class="sxs-lookup"><span data-stu-id="52d9b-128">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="52d9b-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52d9b-129">-Confirm</span></span>
<span data-ttu-id="52d9b-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52d9b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d9b-131">-WhatIf</span></span>
<span data-ttu-id="52d9b-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52d9b-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52d9b-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52d9b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d9b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d9b-134">-DefaultProfile</span></span>
<span data-ttu-id="52d9b-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52d9b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d9b-136">CommonParameters</span></span>
<span data-ttu-id="52d9b-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d9b-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d9b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d9b-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52d9b-139">INPUTS</span></span>

### <span data-ttu-id="52d9b-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-140">ASRProtectableItem</span></span>
<span data-ttu-id="52d9b-141">Parametern ' ProtectableItem ' godkänner värdet av typen ' ASRProtectableItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="52d9b-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="52d9b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52d9b-142">OUTPUTS</span></span>

### <span data-ttu-id="52d9b-143">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="52d9b-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="52d9b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52d9b-144">NOTES</span></span>

## <span data-ttu-id="52d9b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52d9b-145">RELATED LINKS</span></span>

[<span data-ttu-id="52d9b-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="52d9b-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="52d9b-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52d9b-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
