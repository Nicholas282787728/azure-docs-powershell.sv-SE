---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575805"
---
# <span data-ttu-id="fb7fb-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="fb7fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7fb-103">Anger återställnings egenskaper som mål nätverk och virtuell dator storlek för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb7fb-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb7fb-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7fb-106">Cmdleten **set-AzureRmSiteRecoveryReplicationProtectedItem** anger återställnings egenskaper för ett replikerat objekt.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="fb7fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb7fb-107">EXAMPLES</span></span>

## <span data-ttu-id="fb7fb-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb7fb-108">PARAMETERS</span></span>

### <span data-ttu-id="fb7fb-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fb7fb-109">-LicenseType</span></span>
<span data-ttu-id="fb7fb-110">Anger licens typs valet för virtuella datorer med Windows Server som migrerats genom hybrid användning.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7fb-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb7fb-111">-Name</span></span>
<span data-ttu-id="fb7fb-112">Anger namnet på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="fb7fb-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="fb7fb-113">-NicSelectionType</span></span>
<span data-ttu-id="fb7fb-114">Anger de nätverkskort-egenskaper som anges av användaren eller som standard.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="fb7fb-115">Du kan ange NotSelected för att återgå till standardvärdena.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-115">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7fb-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="fb7fb-116">-PrimaryNic</span></span>
<span data-ttu-id="fb7fb-117">Anger NÄTVERKSKORTet för den virtuella dator för vilken denna cmdlet ställer in egenskapen för återställnings nätverk.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="fb7fb-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb7fb-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="fb7fb-119">Anger ID för det Azure Virtual Network som denna cmdlet återställer det skyddade objektet för.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="fb7fb-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="fb7fb-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="fb7fb-121">Anger den statiska IP-adressen som ska kopplas till primär NIC vid återställning.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="fb7fb-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="fb7fb-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="fb7fb-123">Anger namnet på under nätet i det virtuella Recovery Azure-nätverket för vilket denna cmdlet återställer det skyddade objektet.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="fb7fb-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb7fb-125">Anger det skyddade objektet för replikering av Azure Site Recovery-objekt.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7fb-126">-Storlek</span><span class="sxs-lookup"><span data-stu-id="fb7fb-126">-Size</span></span>
<span data-ttu-id="fb7fb-127">Anger storleken på den virtuella återställnings datorn.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="fb7fb-128">Värdet ska vara från den uppsättning storlekar som stöds av virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="fb7fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7fb-129">-DefaultProfile</span></span>
<span data-ttu-id="fb7fb-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7fb-131">CommonParameters</span></span>
<span data-ttu-id="fb7fb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7fb-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7fb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb7fb-134">INPUTS</span></span>

### <span data-ttu-id="fb7fb-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="fb7fb-136">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fb7fb-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="fb7fb-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb7fb-137">OUTPUTS</span></span>

### <span data-ttu-id="fb7fb-138">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fb7fb-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fb7fb-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb7fb-139">NOTES</span></span>

## <span data-ttu-id="fb7fb-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb7fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="fb7fb-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="fb7fb-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="fb7fb-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7fb-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
