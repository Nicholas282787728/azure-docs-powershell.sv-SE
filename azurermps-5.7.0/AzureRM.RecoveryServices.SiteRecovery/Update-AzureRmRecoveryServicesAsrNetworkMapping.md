---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573340"
---
# <span data-ttu-id="f6921-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f6921-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="f6921-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6921-102">SYNOPSIS</span></span>
<span data-ttu-id="f6921-103">Uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f6921-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6921-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6921-104">SYNTAX</span></span>

### <span data-ttu-id="f6921-105">ByNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="f6921-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6921-106">ById</span><span class="sxs-lookup"><span data-stu-id="f6921-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6921-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6921-107">DESCRIPTION</span></span>
<span data-ttu-id="f6921-108">Cmdleten **Update-AzureRmRecoveryServicesAsrNetworkMapping** uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f6921-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="f6921-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6921-109">EXAMPLES</span></span>

### <span data-ttu-id="f6921-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6921-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="f6921-111">Startar uppdateringen av nätverks mappningen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f6921-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f6921-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6921-112">PARAMETERS</span></span>

### <span data-ttu-id="f6921-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6921-113">-Confirm</span></span>
<span data-ttu-id="f6921-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6921-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6921-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6921-115">-DefaultProfile</span></span>
<span data-ttu-id="f6921-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6921-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f6921-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6921-117">-InputObject</span></span>
<span data-ttu-id="f6921-118">Input-objekt: anger det objekt för automatisk nätverks mappning som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="f6921-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6921-119">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="f6921-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="f6921-120">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="f6921-120">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6921-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="f6921-121">-RecoveryNetwork</span></span>
<span data-ttu-id="f6921-122">Anger återställnings nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="f6921-122">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6921-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6921-123">-WhatIf</span></span>
<span data-ttu-id="f6921-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6921-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6921-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6921-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6921-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6921-126">CommonParameters</span></span>
<span data-ttu-id="f6921-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6921-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6921-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6921-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6921-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6921-129">INPUTS</span></span>

### <span data-ttu-id="f6921-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6921-130">None</span></span>

## <span data-ttu-id="f6921-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6921-131">OUTPUTS</span></span>

### <span data-ttu-id="f6921-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f6921-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f6921-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6921-133">NOTES</span></span>

## <span data-ttu-id="f6921-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6921-134">RELATED LINKS</span></span>
