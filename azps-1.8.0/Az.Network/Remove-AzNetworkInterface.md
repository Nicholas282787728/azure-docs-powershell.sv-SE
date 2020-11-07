---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747873"
---
# <span data-ttu-id="a76a2-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a76a2-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="a76a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a76a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a76a2-103">Tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="a76a2-103">Removes a network interface.</span></span>

## <span data-ttu-id="a76a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a76a2-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a76a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a76a2-106">Cmdleten **Remove-AzNetworkInterface** tar bort ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="a76a2-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="a76a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a76a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a76a2-108">Exempel 1: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="a76a2-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="a76a2-109">Det här kommandot tar bort nätverks gränssnittet NetworkInterface1 i resurs gruppen ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a76a2-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="a76a2-110">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a76a2-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="a76a2-111">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="a76a2-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="a76a2-112">Detta kommando tar bort alla nätverks gränssnitt i ResourceGroup1 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a76a2-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="a76a2-113">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a76a2-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="a76a2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a76a2-114">PARAMETERS</span></span>

### <span data-ttu-id="a76a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76a2-115">-AsJob</span></span>
<span data-ttu-id="a76a2-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a76a2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76a2-117">-DefaultProfile</span></span>
<span data-ttu-id="a76a2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a76a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a76a2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a76a2-119">-Force</span></span>
<span data-ttu-id="a76a2-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a76a2-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a76a2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a76a2-121">-Name</span></span>
<span data-ttu-id="a76a2-122">Anger namnet på det nätverks gränssnitt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a76a2-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a76a2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a76a2-123">-PassThru</span></span>
<span data-ttu-id="a76a2-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a76a2-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a76a2-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a76a2-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a76a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a76a2-127">Anger namnet på en resurs grupp som innehåller nätverks gränssnittet som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a76a2-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a76a2-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a76a2-128">-Confirm</span></span>
<span data-ttu-id="a76a2-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a76a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76a2-130">-WhatIf</span></span>
<span data-ttu-id="a76a2-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a76a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76a2-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a76a2-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76a2-133">CommonParameters</span></span>
<span data-ttu-id="a76a2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76a2-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76a2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76a2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a76a2-136">INPUTS</span></span>

### <span data-ttu-id="a76a2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a76a2-137">System.String</span></span>

## <span data-ttu-id="a76a2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a76a2-138">OUTPUTS</span></span>

### <span data-ttu-id="a76a2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a76a2-139">System.Boolean</span></span>

## <span data-ttu-id="a76a2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a76a2-140">NOTES</span></span>

## <span data-ttu-id="a76a2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a76a2-141">RELATED LINKS</span></span>

[<span data-ttu-id="a76a2-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a76a2-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="a76a2-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a76a2-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="a76a2-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a76a2-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


