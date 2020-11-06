---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573622"
---
# <span data-ttu-id="d9a66-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9a66-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d9a66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9a66-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a66-103">Tar bort ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d9a66-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9a66-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9a66-105">DESCRIPTION</span></span>
<span data-ttu-id="d9a66-106">Cmdleten **Remove-AzureRmNetworkInterface** tar bort ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="d9a66-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d9a66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9a66-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a66-108">Exempel 1: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d9a66-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d9a66-109">Det här kommandot tar bort nätverks gränssnittet NetworkInterface1 i resurs gruppen ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d9a66-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d9a66-110">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="d9a66-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d9a66-111">Exempel 2: ta bort ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d9a66-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="d9a66-112">Detta kommando tar bort alla nätverks gränssnitt i ResourceGroup1 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d9a66-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d9a66-113">Eftersom *Force* -parametern används uppmanas användaren inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d9a66-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d9a66-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9a66-114">PARAMETERS</span></span>

### <span data-ttu-id="d9a66-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d9a66-115">-Force</span></span>
<span data-ttu-id="d9a66-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d9a66-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9a66-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9a66-117">-Name</span></span>
<span data-ttu-id="d9a66-118">Anger namnet på det nätverks gränssnitt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d9a66-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9a66-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9a66-119">-PassThru</span></span>
<span data-ttu-id="d9a66-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d9a66-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9a66-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d9a66-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9a66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a66-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9a66-123">Anger namnet på en resurs grupp som innehåller nätverks gränssnittet som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d9a66-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9a66-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9a66-124">-Confirm</span></span>
<span data-ttu-id="d9a66-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9a66-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a66-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a66-126">-WhatIf</span></span>
<span data-ttu-id="d9a66-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9a66-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a66-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9a66-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a66-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a66-129">-DefaultProfile</span></span>
<span data-ttu-id="d9a66-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a66-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9a66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a66-131">CommonParameters</span></span>
<span data-ttu-id="d9a66-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a66-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a66-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a66-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9a66-134">INPUTS</span></span>

## <span data-ttu-id="d9a66-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9a66-135">OUTPUTS</span></span>

## <span data-ttu-id="d9a66-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9a66-136">NOTES</span></span>

## <span data-ttu-id="d9a66-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9a66-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9a66-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9a66-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="d9a66-139">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9a66-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="d9a66-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9a66-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


