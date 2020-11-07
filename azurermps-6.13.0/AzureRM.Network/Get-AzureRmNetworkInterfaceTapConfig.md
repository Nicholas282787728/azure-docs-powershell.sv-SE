---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758323"
---
# <span data-ttu-id="523ff-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="523ff-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="523ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="523ff-102">SYNOPSIS</span></span>
<span data-ttu-id="523ff-103">Hämtar en tryck konfigurations resurs.</span><span class="sxs-lookup"><span data-stu-id="523ff-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="523ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="523ff-104">SYNTAX</span></span>

### <span data-ttu-id="523ff-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="523ff-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="523ff-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="523ff-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="523ff-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="523ff-107">DESCRIPTION</span></span>
<span data-ttu-id="523ff-108">Cmdleten **Get-AzureRmNetworkInterfaceTapConfig** får en Azure knackning-konfiguration för en viss resurs grupp, nätverks gränssnitt och tryck på konfigurations namn eller en lista över konfigurationer i en resurs grupp och ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="523ff-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="523ff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="523ff-109">EXAMPLES</span></span>

### <span data-ttu-id="523ff-110">Exempel 1: Hämta alla tryck konfigurationer för ett visst nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="523ff-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="523ff-111">Det här kommandot får trycka på konfigurationer som lagts till för det angivna nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="523ff-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="523ff-112">Exempel 2: få ett bestämt tryck på konfiguration</span><span class="sxs-lookup"><span data-stu-id="523ff-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="523ff-113">Det här kommandot ger specifik tryck konfiguration som läggs till för det angivna nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="523ff-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="523ff-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="523ff-114">PARAMETERS</span></span>

### <span data-ttu-id="523ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523ff-115">-DefaultProfile</span></span>
<span data-ttu-id="523ff-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="523ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="523ff-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="523ff-117">-Name</span></span>
<span data-ttu-id="523ff-118">Namn på specifik trycknings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="523ff-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523ff-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="523ff-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="523ff-120">Nätverks gränssnittets namn.</span><span class="sxs-lookup"><span data-stu-id="523ff-120">The Network Interface name.</span></span>

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

### <span data-ttu-id="523ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="523ff-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="523ff-122">The resource group name.</span></span>

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

### <span data-ttu-id="523ff-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="523ff-123">-ResourceId</span></span>
<span data-ttu-id="523ff-124">ResourceId för TapConfiguration-resursen</span><span class="sxs-lookup"><span data-stu-id="523ff-124">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="523ff-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="523ff-125">-Confirm</span></span>
<span data-ttu-id="523ff-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="523ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523ff-127">-WhatIf</span></span>
<span data-ttu-id="523ff-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="523ff-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="523ff-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="523ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523ff-130">CommonParameters</span></span>
<span data-ttu-id="523ff-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523ff-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523ff-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="523ff-133">INPUTS</span></span>

### <span data-ttu-id="523ff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="523ff-134">System.String</span></span>

## <span data-ttu-id="523ff-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="523ff-135">OUTPUTS</span></span>

### <span data-ttu-id="523ff-136">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="523ff-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="523ff-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="523ff-137">NOTES</span></span>

## <span data-ttu-id="523ff-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="523ff-138">RELATED LINKS</span></span>
