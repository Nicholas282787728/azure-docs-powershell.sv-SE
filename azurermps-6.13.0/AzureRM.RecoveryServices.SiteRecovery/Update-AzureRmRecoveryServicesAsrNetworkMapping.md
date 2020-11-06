---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: fb92ec38bcbe7addb23f274616cde0fd84ebbafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573931"
---
# <span data-ttu-id="b4f4b-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b4f4b-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b4f4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f4b-103">Uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4f4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4f4b-104">SYNTAX</span></span>

### <span data-ttu-id="b4f4b-105">ByNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="b4f4b-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f4b-106">ById</span><span class="sxs-lookup"><span data-stu-id="b4f4b-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4f4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4f4b-107">DESCRIPTION</span></span>
<span data-ttu-id="b4f4b-108">Cmdleten **Update-AzureRmRecoveryServicesAsrNetworkMapping** uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="b4f4b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4f4b-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f4b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4f4b-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="b4f4b-111">Startar uppdateringen av nätverks mappningen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b4f4b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4f4b-112">PARAMETERS</span></span>

### <span data-ttu-id="b4f4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f4b-113">-DefaultProfile</span></span>
<span data-ttu-id="b4f4b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b4f4b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4f4b-115">-InputObject</span></span>
<span data-ttu-id="b4f4b-116">Input-objekt: anger det objekt för automatisk nätverks mappning som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4b-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="b4f4b-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="b4f4b-118">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4b-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="b4f4b-119">-RecoveryNetwork</span></span>
<span data-ttu-id="b4f4b-120">Anger återställnings nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4f4b-121">-Confirm</span></span>
<span data-ttu-id="b4f4b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f4b-123">-WhatIf</span></span>
<span data-ttu-id="b4f4b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4f4b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f4b-126">CommonParameters</span></span>
<span data-ttu-id="b4f4b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f4b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f4b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f4b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4f4b-129">INPUTS</span></span>

### <span data-ttu-id="b4f4b-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4f4b-130">None</span></span>

## <span data-ttu-id="b4f4b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4f4b-131">OUTPUTS</span></span>

### <span data-ttu-id="b4f4b-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b4f4b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b4f4b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4f4b-133">NOTES</span></span>

## <span data-ttu-id="b4f4b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4f4b-134">RELATED LINKS</span></span>
