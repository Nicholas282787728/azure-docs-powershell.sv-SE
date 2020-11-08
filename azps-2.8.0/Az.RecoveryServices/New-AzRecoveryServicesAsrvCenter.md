---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 8039da508110b47024be75967932719e5436f73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920219"
---
# <span data-ttu-id="492c0-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="492c0-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="492c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="492c0-102">SYNOPSIS</span></span>
<span data-ttu-id="492c0-103">Lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="492c0-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="492c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="492c0-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="492c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="492c0-105">DESCRIPTION</span></span>
<span data-ttu-id="492c0-106">Cmdleten **New-AzRecoveryServicesAsrvCenter** lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="492c0-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="492c0-107">Denna cmdlet registrerar vCenter-servern för identifiering med konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="492c0-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="492c0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="492c0-108">EXAMPLES</span></span>

### <span data-ttu-id="492c0-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="492c0-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="492c0-110">Lägger till en vCenter-Server för att upptäcka objekt som skyddas från.</span><span class="sxs-lookup"><span data-stu-id="492c0-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="492c0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="492c0-111">PARAMETERS</span></span>

### <span data-ttu-id="492c0-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="492c0-112">-Account</span></span>
<span data-ttu-id="492c0-113">Konto för inloggnings uppgifter för användare.</span><span class="sxs-lookup"><span data-stu-id="492c0-113">User login credential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492c0-114">-DefaultProfile</span></span>
<span data-ttu-id="492c0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="492c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="492c0-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="492c0-116">-Fabric</span></span>
<span data-ttu-id="492c0-117">ASR Fabric som motsvarar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="492c0-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="492c0-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="492c0-118">-IpOrHostName</span></span>
<span data-ttu-id="492c0-119">IPv4-adress eller FQDN för vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="492c0-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492c0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="492c0-120">-Name</span></span>
<span data-ttu-id="492c0-121">Ett eget namn för vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="492c0-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492c0-122">-Port</span><span class="sxs-lookup"><span data-stu-id="492c0-122">-Port</span></span>
<span data-ttu-id="492c0-123">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="492c0-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492c0-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="492c0-124">-Confirm</span></span>
<span data-ttu-id="492c0-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="492c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="492c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="492c0-126">-WhatIf</span></span>
<span data-ttu-id="492c0-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="492c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="492c0-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="492c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="492c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492c0-129">CommonParameters</span></span>
<span data-ttu-id="492c0-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492c0-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="492c0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492c0-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="492c0-132">INPUTS</span></span>

### <span data-ttu-id="492c0-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="492c0-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="492c0-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="492c0-134">OUTPUTS</span></span>

### <span data-ttu-id="492c0-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="492c0-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="492c0-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="492c0-136">NOTES</span></span>

## <span data-ttu-id="492c0-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="492c0-137">RELATED LINKS</span></span>