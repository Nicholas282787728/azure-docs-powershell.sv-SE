---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928990"
---
# <span data-ttu-id="e70b3-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e70b3-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="e70b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e70b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e70b3-103">Tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="e70b3-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e70b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e70b3-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e70b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e70b3-106">Cmdleten **Remove-AzureRmNetworkInterface** tar bort ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="e70b3-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="e70b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e70b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e70b3-108">Exempel 1: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="e70b3-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e70b3-109">Det här kommandot tar bort nätverks gränssnittet NetworkInterface1 i resurs gruppen ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="e70b3-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e70b3-110">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e70b3-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="e70b3-111">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="e70b3-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="e70b3-112">Detta kommando tar bort alla nätverks gränssnitt i ResourceGroup1 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e70b3-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e70b3-113">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e70b3-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="e70b3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e70b3-114">PARAMETERS</span></span>

### <span data-ttu-id="e70b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e70b3-115">-AsJob</span></span>
<span data-ttu-id="e70b3-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e70b3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e70b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70b3-117">-DefaultProfile</span></span>
<span data-ttu-id="e70b3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e70b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70b3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e70b3-119">-Force</span></span>
<span data-ttu-id="e70b3-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e70b3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e70b3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e70b3-121">-Name</span></span>
<span data-ttu-id="e70b3-122">Anger namnet på det nätverks gränssnitt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e70b3-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e70b3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e70b3-123">-PassThru</span></span>
<span data-ttu-id="e70b3-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e70b3-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e70b3-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e70b3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e70b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="e70b3-127">Anger namnet på en resurs grupp som innehåller nätverks gränssnittet som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="e70b3-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e70b3-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e70b3-128">-Confirm</span></span>
<span data-ttu-id="e70b3-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e70b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70b3-130">-WhatIf</span></span>
<span data-ttu-id="e70b3-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e70b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70b3-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e70b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70b3-133">CommonParameters</span></span>
<span data-ttu-id="e70b3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70b3-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70b3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70b3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e70b3-136">INPUTS</span></span>

## <span data-ttu-id="e70b3-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e70b3-137">OUTPUTS</span></span>

## <span data-ttu-id="e70b3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e70b3-138">NOTES</span></span>

## <span data-ttu-id="e70b3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e70b3-139">RELATED LINKS</span></span>

[<span data-ttu-id="e70b3-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e70b3-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="e70b3-141">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e70b3-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="e70b3-142">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e70b3-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


