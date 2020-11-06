---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573360"
---
# <span data-ttu-id="8650e-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8650e-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8650e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8650e-102">SYNOPSIS</span></span>
<span data-ttu-id="8650e-103">Lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="8650e-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8650e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8650e-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8650e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8650e-105">DESCRIPTION</span></span>
<span data-ttu-id="8650e-106">Cmdleten **New-AzureRmRecoveryServicesAsrvCenter** lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="8650e-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="8650e-107">Denna cmdlet registrerar vCenter-servern för identifiering med konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="8650e-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="8650e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8650e-108">EXAMPLES</span></span>

### <span data-ttu-id="8650e-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8650e-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="8650e-110">Lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="8650e-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="8650e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8650e-111">PARAMETERS</span></span>

### <span data-ttu-id="8650e-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="8650e-112">-Account</span></span>
<span data-ttu-id="8650e-113">Användar inloggning creadential-konto.</span><span class="sxs-lookup"><span data-stu-id="8650e-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8650e-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8650e-114">-Confirm</span></span>
<span data-ttu-id="8650e-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8650e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8650e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8650e-116">-DefaultProfile</span></span>
<span data-ttu-id="8650e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8650e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8650e-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8650e-118">-Fabric</span></span>
<span data-ttu-id="8650e-119">ASR Fabric som motsvarar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="8650e-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8650e-120">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="8650e-120">-IpOrHostName</span></span>
<span data-ttu-id="8650e-121">IPv4-adress eller FQDN för vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="8650e-121">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8650e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8650e-122">-Name</span></span>
<span data-ttu-id="8650e-123">Ett eget namn för vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="8650e-123">A friendly name for the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8650e-124">-Port</span><span class="sxs-lookup"><span data-stu-id="8650e-124">-Port</span></span>
<span data-ttu-id="8650e-125">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="8650e-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8650e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8650e-126">-WhatIf</span></span>
<span data-ttu-id="8650e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8650e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8650e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8650e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8650e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8650e-129">CommonParameters</span></span>
<span data-ttu-id="8650e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8650e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8650e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8650e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8650e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8650e-132">INPUTS</span></span>

### <span data-ttu-id="8650e-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8650e-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8650e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8650e-134">OUTPUTS</span></span>

### <span data-ttu-id="8650e-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8650e-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8650e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8650e-136">NOTES</span></span>

## <span data-ttu-id="8650e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8650e-137">RELATED LINKS</span></span>
