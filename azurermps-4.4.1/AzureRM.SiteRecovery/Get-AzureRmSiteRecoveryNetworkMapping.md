---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577420"
---
# <span data-ttu-id="44043-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="44043-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="44043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44043-102">SYNOPSIS</span></span>
<span data-ttu-id="44043-103">Hämtar information om nätverks mappningar för webbplats återställning för det aktuella valvet.</span><span class="sxs-lookup"><span data-stu-id="44043-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44043-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44043-104">SYNTAX</span></span>

### <span data-ttu-id="44043-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="44043-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44043-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="44043-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44043-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="44043-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44043-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="44043-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44043-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="44043-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44043-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44043-110">DESCRIPTION</span></span>
<span data-ttu-id="44043-111">Cmdleten **Get-AzureRmSiteRecoveryNetworkMapping** hämtar information om nätverks mappningar för Azure Site Recovery för det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="44043-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="44043-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44043-112">EXAMPLES</span></span>

## <span data-ttu-id="44043-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44043-113">PARAMETERS</span></span>

### <span data-ttu-id="44043-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="44043-114">-Azure</span></span>
<span data-ttu-id="44043-115">Visar att kommandot får en lista över nätverks mappningar för nätverk på den primära servern som mappats till virtuella Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="44043-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44043-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="44043-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44043-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="44043-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44043-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="44043-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44043-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="44043-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44043-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44043-120">-DefaultProfile</span></span>
<span data-ttu-id="44043-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44043-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44043-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44043-122">CommonParameters</span></span>
<span data-ttu-id="44043-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44043-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44043-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44043-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44043-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44043-125">INPUTS</span></span>

### <span data-ttu-id="44043-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="44043-126">ASRFabric</span></span>
<span data-ttu-id="44043-127">Parametern ' PrimaryFabric ' godkänner värdet av typen ' ASRFabric ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="44043-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="44043-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="44043-128">ASRServer</span></span>
<span data-ttu-id="44043-129">Parametern ' PrimaryServer ' godkänner värdet av typen ' ASRServer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="44043-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="44043-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44043-130">OUTPUTS</span></span>

### <span data-ttu-id="44043-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="44043-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="44043-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44043-132">NOTES</span></span>

## <span data-ttu-id="44043-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44043-133">RELATED LINKS</span></span>

[<span data-ttu-id="44043-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="44043-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="44043-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="44043-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
