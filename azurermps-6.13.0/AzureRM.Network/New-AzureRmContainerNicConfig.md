---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758160"
---
# <span data-ttu-id="2b23d-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2b23d-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="2b23d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b23d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b23d-103">Skapar ett nytt konfigurations objekt för behållarens nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="2b23d-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b23d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b23d-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b23d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b23d-105">DESCRIPTION</span></span>
<span data-ttu-id="2b23d-106">Cmdleten **New-AzureRmNetworkProfileContainerNicConfig** skapar ett nytt konfigurations objekt för behållaren för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="2b23d-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="2b23d-107">Det här objektet bestämmer egenskaperna för behållar nätverks-interfacs som skapats som refererar till den överordnade nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="2b23d-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="2b23d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b23d-108">EXAMPLES</span></span>

### <span data-ttu-id="2b23d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2b23d-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="2b23d-110">Det första kommandot skapar en tom konfiguration för nätverks gränssnitt för behållare.</span><span class="sxs-lookup"><span data-stu-id="2b23d-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="2b23d-111">Den andra skapar en ny nätverks profil och skickar den tidigare skapade konfigurationen för nätverks gränssnitt för behållare som ett argument till New-NetworkProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b23d-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="2b23d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b23d-112">PARAMETERS</span></span>

### <span data-ttu-id="2b23d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b23d-113">-DefaultProfile</span></span>
<span data-ttu-id="2b23d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b23d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b23d-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b23d-115">-IpConfiguration</span></span>
<span data-ttu-id="2b23d-116">{{Fill IpConfiguration}}</span><span class="sxs-lookup"><span data-stu-id="2b23d-116">{{Fill IpConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b23d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b23d-117">-Name</span></span>
<span data-ttu-id="2b23d-118">Namn på behållarens nätverks gränssnitts konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b23d-118">Name of the container network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b23d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b23d-119">-Confirm</span></span>
<span data-ttu-id="2b23d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b23d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b23d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b23d-121">-WhatIf</span></span>
<span data-ttu-id="2b23d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b23d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b23d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b23d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b23d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b23d-124">CommonParameters</span></span>
<span data-ttu-id="2b23d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b23d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b23d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b23d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b23d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b23d-127">INPUTS</span></span>

### <span data-ttu-id="2b23d-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSIPConfigurationProfile, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b23d-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b23d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b23d-129">OUTPUTS</span></span>

### <span data-ttu-id="2b23d-130">Microsoft. Azure. commands. Networks. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b23d-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="2b23d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b23d-131">NOTES</span></span>

## <span data-ttu-id="2b23d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b23d-132">RELATED LINKS</span></span>
