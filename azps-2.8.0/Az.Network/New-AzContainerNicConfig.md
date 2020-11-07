---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: aaace7e8bb7d1f2ed57ebad28f7b5a3399f0e190
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919105"
---
# <span data-ttu-id="1a84a-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1a84a-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="1a84a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a84a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a84a-103">Skapar ett nytt konfigurations objekt för behållarens nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="1a84a-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="1a84a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a84a-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a84a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a84a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a84a-106">Cmdleten **New-AzContainerNicConfig** skapar ett nytt konfigurations objekt för behållaren för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="1a84a-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="1a84a-107">Det här objektet bestämmer egenskaperna för behållar nätverks gränssnittet som skapas och den överordnade nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="1a84a-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="1a84a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a84a-108">EXAMPLES</span></span>

### <span data-ttu-id="1a84a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a84a-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="1a84a-110">Det första kommandot skapar en tom konfiguration för nätverks gränssnitt för behållare.</span><span class="sxs-lookup"><span data-stu-id="1a84a-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="1a84a-111">Den andra skapar en ny nätverks profil och skickar den tidigare skapade konfigurationen för nätverks gränssnitt för behållare som ett argument till New-NetworkProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a84a-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="1a84a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a84a-112">PARAMETERS</span></span>

### <span data-ttu-id="1a84a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a84a-113">-DefaultProfile</span></span>
<span data-ttu-id="1a84a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a84a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a84a-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a84a-115">-IpConfiguration</span></span>
<span data-ttu-id="1a84a-116">Insamling av IP-konfigurationsinställningar som avgör vilka IP-konfigurationer som skapas när en container-NIC instansieras från den här nätverks gränssnitts konfigurationen</span><span class="sxs-lookup"><span data-stu-id="1a84a-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

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

### <span data-ttu-id="1a84a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a84a-117">-Name</span></span>
<span data-ttu-id="1a84a-118">Namn på behållarens nätverks gränssnitts konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1a84a-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="1a84a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a84a-119">-Confirm</span></span>
<span data-ttu-id="1a84a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a84a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a84a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a84a-121">-WhatIf</span></span>
<span data-ttu-id="1a84a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a84a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a84a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a84a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a84a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a84a-124">CommonParameters</span></span>
<span data-ttu-id="1a84a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a84a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a84a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a84a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a84a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a84a-127">INPUTS</span></span>

### <span data-ttu-id="1a84a-128">Microsoft. Azure. commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="1a84a-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="1a84a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a84a-129">OUTPUTS</span></span>

### <span data-ttu-id="1a84a-130">Microsoft. Azure. commands. Networks. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a84a-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="1a84a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a84a-131">NOTES</span></span>

## <span data-ttu-id="1a84a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a84a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a84a-133">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1a84a-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
