---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572700"
---
# <span data-ttu-id="b8a02-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b8a02-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="b8a02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8a02-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a02-103">Anger mål tillstånd för en tryck konfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a02-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8a02-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8a02-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a02-106">**Set-AzureRmNetworkInterfaceTapConfig** anger mål tillståndet för ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="b8a02-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="b8a02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8a02-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a02-108">Exempel 1: Ange TapConfiguration med uppdaterat TapConfig-namn</span><span class="sxs-lookup"><span data-stu-id="b8a02-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="b8a02-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8a02-109">PARAMETERS</span></span>

### <span data-ttu-id="b8a02-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8a02-110">-AsJob</span></span>
<span data-ttu-id="b8a02-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b8a02-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8a02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a02-112">-DefaultProfile</span></span>
<span data-ttu-id="b8a02-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a02-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a02-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b8a02-114">-Force</span></span>
<span data-ttu-id="b8a02-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b8a02-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b8a02-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b8a02-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="b8a02-117">NetworkInterface tryck på configurtion</span><span class="sxs-lookup"><span data-stu-id="b8a02-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="b8a02-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8a02-118">-Confirm</span></span>
<span data-ttu-id="b8a02-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8a02-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a02-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a02-120">-WhatIf</span></span>
<span data-ttu-id="b8a02-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8a02-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a02-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8a02-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a02-123">CommonParameters</span></span>
<span data-ttu-id="b8a02-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a02-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a02-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a02-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8a02-126">INPUTS</span></span>

### <span data-ttu-id="b8a02-127">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a02-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="b8a02-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8a02-128">OUTPUTS</span></span>

### <span data-ttu-id="b8a02-129">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b8a02-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b8a02-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8a02-130">NOTES</span></span>

## <span data-ttu-id="b8a02-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8a02-131">RELATED LINKS</span></span>
