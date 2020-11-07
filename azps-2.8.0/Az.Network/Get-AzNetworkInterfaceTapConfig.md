---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918736"
---
# <span data-ttu-id="5353f-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5353f-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="5353f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5353f-102">SYNOPSIS</span></span>
<span data-ttu-id="5353f-103">Hämtar en tryck konfigurations resurs.</span><span class="sxs-lookup"><span data-stu-id="5353f-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="5353f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5353f-104">SYNTAX</span></span>

### <span data-ttu-id="5353f-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5353f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5353f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5353f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5353f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5353f-107">DESCRIPTION</span></span>
<span data-ttu-id="5353f-108">Cmdleten **Get-AzNetworkInterfaceTapConfig** får en Azure knackning-konfiguration för en viss resurs grupp, nätverks gränssnitt och tryck på konfigurations namn eller en lista över konfigurationer i en resurs grupp och ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="5353f-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="5353f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5353f-109">EXAMPLES</span></span>

### <span data-ttu-id="5353f-110">Exempel 1: Hämta alla tryck konfigurationer för ett visst nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="5353f-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="5353f-111">Det här kommandot får trycka på konfigurationer som lagts till för det angivna nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="5353f-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="5353f-112">Exempel 2: få ett bestämt tryck på konfiguration</span><span class="sxs-lookup"><span data-stu-id="5353f-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="5353f-113">Det här kommandot ger specifik tryck konfiguration som läggs till för det angivna nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="5353f-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="5353f-114">Exempel 3: få en specifik trycknings konfiguration</span><span class="sxs-lookup"><span data-stu-id="5353f-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="5353f-115">Det här kommandot får trycka på konfigurationer som lagts till för det angivna nätverks gränssnittet med namn som börjar med "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="5353f-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="5353f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5353f-116">PARAMETERS</span></span>

### <span data-ttu-id="5353f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5353f-117">-DefaultProfile</span></span>
<span data-ttu-id="5353f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5353f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5353f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5353f-119">-Name</span></span>
<span data-ttu-id="5353f-120">Namn på specifik trycknings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5353f-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5353f-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5353f-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="5353f-122">Nätverks gränssnittets namn.</span><span class="sxs-lookup"><span data-stu-id="5353f-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5353f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5353f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5353f-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5353f-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5353f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5353f-125">-ResourceId</span></span>
<span data-ttu-id="5353f-126">ResourceId för TapConfiguration-resursen</span><span class="sxs-lookup"><span data-stu-id="5353f-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5353f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5353f-127">-Confirm</span></span>
<span data-ttu-id="5353f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5353f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5353f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5353f-129">-WhatIf</span></span>
<span data-ttu-id="5353f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5353f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5353f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5353f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5353f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5353f-132">CommonParameters</span></span>
<span data-ttu-id="5353f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5353f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5353f-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5353f-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5353f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5353f-135">INPUTS</span></span>

### <span data-ttu-id="5353f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5353f-136">System.String</span></span>

## <span data-ttu-id="5353f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5353f-137">OUTPUTS</span></span>

### <span data-ttu-id="5353f-138">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="5353f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="5353f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5353f-139">NOTES</span></span>

## <span data-ttu-id="5353f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5353f-140">RELATED LINKS</span></span>

[<span data-ttu-id="5353f-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5353f-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5353f-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5353f-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5353f-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5353f-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
