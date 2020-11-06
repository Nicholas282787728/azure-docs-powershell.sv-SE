---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572696"
---
# <span data-ttu-id="b0d01-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b0d01-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="b0d01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0d01-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d01-103">Anger mål tillstånd för en befintlig nätverks profil</span><span class="sxs-lookup"><span data-stu-id="b0d01-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0d01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0d01-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0d01-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d01-106">Cmdleten **set-AzureRmPublicIpPrefix** anger mål tillståndet för en nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="b0d01-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="b0d01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0d01-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d01-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0d01-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="b0d01-109">Det första kommandot får en befintlig nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="b0d01-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="b0d01-110">Det andra kommandot uppdaterar en tagg och den tredje lägger till en nätverks gränssnitts konfiguration i nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="b0d01-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="b0d01-111">Det fjärde kommandot uppdaterar nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="b0d01-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="b0d01-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0d01-112">PARAMETERS</span></span>

### <span data-ttu-id="b0d01-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0d01-113">-AsJob</span></span>
<span data-ttu-id="b0d01-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0d01-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0d01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d01-115">-DefaultProfile</span></span>
<span data-ttu-id="b0d01-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d01-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b0d01-117">-NetworkProfile</span></span>
<span data-ttu-id="b0d01-118">Nätverks profilen</span><span class="sxs-lookup"><span data-stu-id="b0d01-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d01-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0d01-119">-Confirm</span></span>
<span data-ttu-id="b0d01-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0d01-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d01-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d01-121">-WhatIf</span></span>
<span data-ttu-id="b0d01-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0d01-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0d01-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0d01-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d01-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d01-124">CommonParameters</span></span>
<span data-ttu-id="b0d01-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d01-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d01-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d01-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d01-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0d01-127">INPUTS</span></span>

### <span data-ttu-id="b0d01-128">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b0d01-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b0d01-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0d01-129">OUTPUTS</span></span>

### <span data-ttu-id="b0d01-130">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b0d01-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="b0d01-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0d01-131">NOTES</span></span>

## <span data-ttu-id="b0d01-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0d01-132">RELATED LINKS</span></span>
