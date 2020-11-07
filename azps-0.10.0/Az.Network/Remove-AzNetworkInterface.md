---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 403c41de0359f2d857d2c86b772e4af419640f2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922025"
---
# <span data-ttu-id="d56b9-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56b9-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="d56b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d56b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d56b9-103">Tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d56b9-103">Removes a network interface.</span></span>

## <span data-ttu-id="d56b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d56b9-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d56b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d56b9-106">Cmdleten **Remove-AzNetworkInterface** tar bort ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="d56b9-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d56b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d56b9-107">EXAMPLES</span></span>

### <span data-ttu-id="d56b9-108">Exempel 1: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d56b9-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d56b9-109">Det här kommandot tar bort nätverks gränssnittet NetworkInterface1 i resurs gruppen ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d56b9-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d56b9-110">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="d56b9-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d56b9-111">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d56b9-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="d56b9-112">Detta kommando tar bort alla nätverks gränssnitt i ResourceGroup1 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d56b9-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d56b9-113">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d56b9-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d56b9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d56b9-114">PARAMETERS</span></span>

### <span data-ttu-id="d56b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d56b9-115">-AsJob</span></span>
<span data-ttu-id="d56b9-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d56b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d56b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56b9-117">-DefaultProfile</span></span>
<span data-ttu-id="d56b9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d56b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d56b9-119">-Force</span></span>
<span data-ttu-id="d56b9-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d56b9-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d56b9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d56b9-121">-Name</span></span>
<span data-ttu-id="d56b9-122">Anger namnet på det nätverks gränssnitt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d56b9-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d56b9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d56b9-123">-PassThru</span></span>
<span data-ttu-id="d56b9-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d56b9-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d56b9-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d56b9-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d56b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="d56b9-127">Anger namnet på en resurs grupp som innehåller nätverks gränssnittet som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d56b9-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d56b9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d56b9-128">-Confirm</span></span>
<span data-ttu-id="d56b9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d56b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56b9-130">-WhatIf</span></span>
<span data-ttu-id="d56b9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d56b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56b9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d56b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56b9-133">CommonParameters</span></span>
<span data-ttu-id="d56b9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56b9-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56b9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56b9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d56b9-136">INPUTS</span></span>

## <span data-ttu-id="d56b9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d56b9-137">OUTPUTS</span></span>

## <span data-ttu-id="d56b9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d56b9-138">NOTES</span></span>

## <span data-ttu-id="d56b9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d56b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d56b9-140">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56b9-140">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d56b9-141">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56b9-141">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d56b9-142">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56b9-142">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


