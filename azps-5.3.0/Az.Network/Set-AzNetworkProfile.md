---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525771"
---
# <span data-ttu-id="7f158-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="7f158-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f158-102">SYNOPSIS</span></span>
<span data-ttu-id="7f158-103">Uppdaterar en nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="7f158-103">Updates a network profile.</span></span>

## <span data-ttu-id="7f158-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f158-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f158-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f158-105">DESCRIPTION</span></span>
<span data-ttu-id="7f158-106">Cmdleten **set-AzPublicIpPrefix** uppdaterar en nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="7f158-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="7f158-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f158-107">EXAMPLES</span></span>

### <span data-ttu-id="7f158-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f158-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="7f158-109">Det första kommandot får en befintlig nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="7f158-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="7f158-110">Det andra kommandot uppdaterar en tagg och den tredje lägger till en nätverks gränssnitts konfiguration i nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="7f158-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="7f158-111">Det fjärde kommandot uppdaterar nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="7f158-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="7f158-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f158-112">PARAMETERS</span></span>

### <span data-ttu-id="7f158-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f158-113">-AsJob</span></span>
<span data-ttu-id="7f158-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7f158-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f158-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-115">-DefaultProfile</span></span>
<span data-ttu-id="7f158-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f158-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f158-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-117">-NetworkProfile</span></span>
<span data-ttu-id="7f158-118">Nätverks profilen</span><span class="sxs-lookup"><span data-stu-id="7f158-118">The network profile</span></span>

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

### <span data-ttu-id="7f158-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f158-119">-Confirm</span></span>
<span data-ttu-id="7f158-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f158-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f158-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f158-121">-WhatIf</span></span>
<span data-ttu-id="7f158-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f158-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f158-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f158-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f158-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f158-124">CommonParameters</span></span>
<span data-ttu-id="7f158-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f158-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f158-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f158-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f158-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f158-127">INPUTS</span></span>

### <span data-ttu-id="7f158-128">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7f158-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f158-129">OUTPUTS</span></span>

### <span data-ttu-id="7f158-130">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7f158-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f158-131">NOTES</span></span>

## <span data-ttu-id="7f158-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f158-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f158-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="7f158-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="7f158-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7f158-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
