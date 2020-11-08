---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270071"
---
# <span data-ttu-id="4dfc7-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="4dfc7-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="4dfc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dfc7-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfc7-103">Uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="4dfc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dfc7-104">SYNTAX</span></span>

### <span data-ttu-id="4dfc7-105">ByNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="4dfc7-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dfc7-106">ById</span><span class="sxs-lookup"><span data-stu-id="4dfc7-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dfc7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dfc7-107">DESCRIPTION</span></span>
<span data-ttu-id="4dfc7-108">Cmdleten **Update-AzRecoveryServicesAsrNetworkMapping** uppdaterar den angivna nätverks mappningen för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="4dfc7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dfc7-109">EXAMPLES</span></span>

### <span data-ttu-id="4dfc7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4dfc7-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="4dfc7-111">Startar uppdateringen av nätverks mappningen med de angivna parametrarna och returnerar det ASR-jobb som används för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4dfc7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dfc7-112">PARAMETERS</span></span>

### <span data-ttu-id="4dfc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfc7-113">-DefaultProfile</span></span>
<span data-ttu-id="4dfc7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfc7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dfc7-115">-InputObject</span></span>
<span data-ttu-id="4dfc7-116">Input-objekt: anger det objekt för automatisk nätverks mappning som motsvarar nätverks mappningen för automatisk system återställning.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="4dfc7-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="4dfc7-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="4dfc7-118">Anger återställnings-nätverks-ID för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="4dfc7-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="4dfc7-119">-RecoveryNetwork</span></span>
<span data-ttu-id="4dfc7-120">Anger återställnings nätverks objekt för nätverks mappningen.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="4dfc7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dfc7-121">-Confirm</span></span>
<span data-ttu-id="4dfc7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfc7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfc7-123">-WhatIf</span></span>
<span data-ttu-id="4dfc7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dfc7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfc7-126">CommonParameters</span></span>
<span data-ttu-id="4dfc7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfc7-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dfc7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfc7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dfc7-129">INPUTS</span></span>

### <span data-ttu-id="4dfc7-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="4dfc7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="4dfc7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dfc7-131">OUTPUTS</span></span>

### <span data-ttu-id="4dfc7-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4dfc7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4dfc7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dfc7-133">NOTES</span></span>

## <span data-ttu-id="4dfc7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dfc7-134">RELATED LINKS</span></span>
