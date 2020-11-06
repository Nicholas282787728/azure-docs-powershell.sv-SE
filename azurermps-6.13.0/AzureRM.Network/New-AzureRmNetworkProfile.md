---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576880"
---
# <span data-ttu-id="7c15c-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c15c-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="7c15c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c15c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c15c-103">Skapar en ny nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="7c15c-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c15c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c15c-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c15c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c15c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c15c-106">Cmdleten **New-AzureRmNetworkProfile** skapar en ny nätverks profil på toppnivå resursen.</span><span class="sxs-lookup"><span data-stu-id="7c15c-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="7c15c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c15c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c15c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c15c-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="7c15c-109">Då skapas en ny nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="7c15c-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="7c15c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c15c-110">PARAMETERS</span></span>

### <span data-ttu-id="7c15c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c15c-111">-AsJob</span></span>
<span data-ttu-id="7c15c-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7c15c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c15c-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7c15c-113">-ContainerNicConfig</span></span>
<span data-ttu-id="7c15c-114">Konfiguration av behållare för nätverks gränssnitt att lägga till i den här nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="7c15c-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c15c-115">-DefaultProfile</span></span>
<span data-ttu-id="7c15c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c15c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c15c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7c15c-117">-Force</span></span>
<span data-ttu-id="7c15c-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="7c15c-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7c15c-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c15c-119">-Location</span></span>
<span data-ttu-id="7c15c-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="7c15c-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c15c-121">-Name</span></span>
<span data-ttu-id="7c15c-122">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="7c15c-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c15c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c15c-124">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="7c15c-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15c-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7c15c-125">-Tag</span></span>
<span data-ttu-id="7c15c-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7c15c-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c15c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c15c-127">-Confirm</span></span>
<span data-ttu-id="7c15c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c15c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c15c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c15c-129">-WhatIf</span></span>
<span data-ttu-id="7c15c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c15c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c15c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c15c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c15c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c15c-132">CommonParameters</span></span>
<span data-ttu-id="7c15c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c15c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c15c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c15c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c15c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c15c-135">INPUTS</span></span>

### <span data-ttu-id="7c15c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7c15c-136">System.String</span></span>

### <span data-ttu-id="7c15c-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7c15c-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7c15c-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSContainerNetworkInterface, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7c15c-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7c15c-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7c15c-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7c15c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c15c-140">OUTPUTS</span></span>

### <span data-ttu-id="7c15c-141">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c15c-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7c15c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c15c-142">NOTES</span></span>

## <span data-ttu-id="7c15c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c15c-143">RELATED LINKS</span></span>
