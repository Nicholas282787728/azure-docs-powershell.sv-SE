---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582931"
---
# <span data-ttu-id="a66de-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a66de-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="a66de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a66de-102">SYNOPSIS</span></span>
<span data-ttu-id="a66de-103">Anger återställnings sidans alternativ för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="a66de-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a66de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a66de-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a66de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a66de-105">DESCRIPTION</span></span>
<span data-ttu-id="a66de-106">Cmdleten **set-AzureRmSiteRecoveryVM** anger återställnings skydds alternativen, till exempel storlek på virtuell dator och Återställ virtuellt dator nätverk, för entiteter för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="a66de-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="a66de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a66de-107">EXAMPLES</span></span>

## <span data-ttu-id="a66de-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a66de-108">PARAMETERS</span></span>

### <span data-ttu-id="a66de-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66de-109">-DefaultProfile</span></span>
<span data-ttu-id="a66de-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a66de-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a66de-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="a66de-111">-Name</span></span>
<span data-ttu-id="a66de-112">Anger namnet på den virtuella mål datorn.</span><span class="sxs-lookup"><span data-stu-id="a66de-112">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="a66de-113">-NicSelectionType</span></span>
<span data-ttu-id="a66de-114">Anger egenskaperna för val av nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="a66de-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="a66de-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a66de-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a66de-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="a66de-116">NotSelected</span></span>
- <span data-ttu-id="a66de-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="a66de-117">SelectedByUser</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="a66de-118">-PrimaryNic</span></span>
<span data-ttu-id="a66de-119">Anger det primära nätverkskortet.</span><span class="sxs-lookup"><span data-stu-id="a66de-119">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="a66de-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="a66de-121">Anger återställnings nätverkets ID.</span><span class="sxs-lookup"><span data-stu-id="a66de-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a66de-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a66de-123">Anger den statiska IP-adress som är kopplad till primär nätverkskortets styrenhet vid återställning.</span><span class="sxs-lookup"><span data-stu-id="a66de-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="a66de-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="a66de-125">Anger det Azure Virtual Network under nätets namn som du vill ansluta den primära nätverkskort kontrollen till vid återställning.</span><span class="sxs-lookup"><span data-stu-id="a66de-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-126">-Storlek</span><span class="sxs-lookup"><span data-stu-id="a66de-126">-Size</span></span>
<span data-ttu-id="a66de-127">Anger storleken på den virtuella datorns mål.</span><span class="sxs-lookup"><span data-stu-id="a66de-127">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a66de-128">-VirtualMachine</span></span>
<span data-ttu-id="a66de-129">Anger det virtuella datorobjektet för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="a66de-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a66de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66de-130">CommonParameters</span></span>
<span data-ttu-id="a66de-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66de-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66de-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a66de-133">INPUTS</span></span>

### <span data-ttu-id="a66de-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a66de-134">ASRVirtualMachine</span></span>
<span data-ttu-id="a66de-135">Parametern ' VirtualMachine ' godkänner värdet av typen ' ASRVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a66de-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="a66de-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a66de-136">OUTPUTS</span></span>

### <span data-ttu-id="a66de-137">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a66de-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a66de-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a66de-138">NOTES</span></span>

## <span data-ttu-id="a66de-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a66de-139">RELATED LINKS</span></span>

[<span data-ttu-id="a66de-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a66de-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
