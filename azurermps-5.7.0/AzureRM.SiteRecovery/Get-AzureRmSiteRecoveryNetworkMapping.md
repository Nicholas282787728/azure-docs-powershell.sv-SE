---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1e7e53d4f14649ac5cb8691a1e3d938809658771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757219"
---
# <span data-ttu-id="1c50f-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1c50f-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="1c50f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c50f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c50f-103">Hämtar information om nätverks mappningar för webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="1c50f-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c50f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c50f-104">SYNTAX</span></span>

### <span data-ttu-id="1c50f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="1c50f-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c50f-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1c50f-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c50f-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1c50f-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c50f-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="1c50f-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c50f-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="1c50f-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c50f-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c50f-110">DESCRIPTION</span></span>
<span data-ttu-id="1c50f-111">Cmdleten **Get-AzureRmSiteRecoveryNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="1c50f-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="1c50f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c50f-112">EXAMPLES</span></span>

## <span data-ttu-id="1c50f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c50f-113">PARAMETERS</span></span>

### <span data-ttu-id="1c50f-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="1c50f-114">-Azure</span></span>
<span data-ttu-id="1c50f-115">Visar att kommandot får en lista över nätverks mappningar för nätverk på den primära servern som mappats till virtuella Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="1c50f-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c50f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c50f-116">-DefaultProfile</span></span>
<span data-ttu-id="1c50f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c50f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c50f-118">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1c50f-118">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c50f-119">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="1c50f-119">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c50f-120">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1c50f-120">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c50f-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1c50f-121">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c50f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c50f-122">CommonParameters</span></span>
<span data-ttu-id="1c50f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c50f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c50f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c50f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c50f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c50f-125">INPUTS</span></span>

### <span data-ttu-id="1c50f-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1c50f-126">ASRFabric</span></span>
<span data-ttu-id="1c50f-127">Parametern ' PrimaryFabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1c50f-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="1c50f-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="1c50f-128">ASRServer</span></span>
<span data-ttu-id="1c50f-129">Parametern ' PrimaryServer ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1c50f-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="1c50f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c50f-130">OUTPUTS</span></span>

### <span data-ttu-id="1c50f-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="1c50f-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="1c50f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c50f-132">NOTES</span></span>

## <span data-ttu-id="1c50f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c50f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1c50f-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1c50f-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="1c50f-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1c50f-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
