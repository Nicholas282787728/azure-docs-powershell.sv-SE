---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271743"
---
# <span data-ttu-id="e2d38-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d38-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="e2d38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2d38-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d38-103">Uppdaterar en tryck konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e2d38-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="e2d38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2d38-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2d38-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d38-106">**Set-AzNetworkInterfaceTapConfig** uppdaterar en skärm konfiguration för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e2d38-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="e2d38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2d38-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d38-108">Exempel 1: Ange TapConfiguration med uppdaterat TapConfig-namn</span><span class="sxs-lookup"><span data-stu-id="e2d38-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="e2d38-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2d38-109">PARAMETERS</span></span>

### <span data-ttu-id="e2d38-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2d38-110">-AsJob</span></span>
<span data-ttu-id="e2d38-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e2d38-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2d38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d38-112">-DefaultProfile</span></span>
<span data-ttu-id="e2d38-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d38-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d38-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e2d38-114">-Force</span></span>
<span data-ttu-id="e2d38-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2d38-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e2d38-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d38-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="e2d38-117">NetworkInterface tryck på konfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d38-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d38-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2d38-118">-Confirm</span></span>
<span data-ttu-id="e2d38-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2d38-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d38-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d38-120">-WhatIf</span></span>
<span data-ttu-id="e2d38-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2d38-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d38-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2d38-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d38-123">CommonParameters</span></span>
<span data-ttu-id="e2d38-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d38-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d38-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d38-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2d38-126">INPUTS</span></span>

### <span data-ttu-id="e2d38-127">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d38-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="e2d38-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2d38-128">OUTPUTS</span></span>

### <span data-ttu-id="e2d38-129">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2d38-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e2d38-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2d38-130">NOTES</span></span>

## <span data-ttu-id="e2d38-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2d38-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2d38-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d38-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e2d38-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d38-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e2d38-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2d38-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)