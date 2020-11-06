---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574256"
---
# <span data-ttu-id="a403a-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a403a-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="a403a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a403a-102">SYNOPSIS</span></span>
<span data-ttu-id="a403a-103">Tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a403a-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a403a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a403a-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a403a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a403a-105">DESCRIPTION</span></span>
<span data-ttu-id="a403a-106">Cmdleten **Remove-AzureRmNetworkInterface** tar bort ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="a403a-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="a403a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a403a-107">EXAMPLES</span></span>

### <span data-ttu-id="a403a-108">Exempel 1: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="a403a-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="a403a-109">Det här kommandot tar bort nätverks gränssnittet NetworkInterface1 i resurs gruppen ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a403a-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="a403a-110">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a403a-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="a403a-111">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="a403a-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="a403a-112">Detta kommando tar bort alla nätverks gränssnitt i ResourceGroup1 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a403a-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="a403a-113">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a403a-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="a403a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a403a-114">PARAMETERS</span></span>

### <span data-ttu-id="a403a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a403a-115">-AsJob</span></span>
<span data-ttu-id="a403a-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a403a-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a403a-117">-DefaultProfile</span></span>
<span data-ttu-id="a403a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a403a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a403a-119">-Force</span></span>
<span data-ttu-id="a403a-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a403a-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a403a-121">-Name</span></span>
<span data-ttu-id="a403a-122">Anger namnet på det nätverks gränssnitt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a403a-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a403a-123">-PassThru</span></span>
<span data-ttu-id="a403a-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a403a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a403a-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a403a-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a403a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a403a-127">Anger namnet på en resurs grupp som innehåller nätverks gränssnittet som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a403a-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a403a-128">-Confirm</span></span>
<span data-ttu-id="a403a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a403a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a403a-130">-WhatIf</span></span>
<span data-ttu-id="a403a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a403a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a403a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a403a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a403a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a403a-133">CommonParameters</span></span>
<span data-ttu-id="a403a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a403a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a403a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a403a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a403a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a403a-136">INPUTS</span></span>

### <span data-ttu-id="a403a-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="a403a-137">None</span></span>
<span data-ttu-id="a403a-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a403a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a403a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a403a-139">OUTPUTS</span></span>

## <span data-ttu-id="a403a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a403a-140">NOTES</span></span>

## <span data-ttu-id="a403a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a403a-141">RELATED LINKS</span></span>

[<span data-ttu-id="a403a-142">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a403a-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="a403a-143">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a403a-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="a403a-144">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a403a-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


