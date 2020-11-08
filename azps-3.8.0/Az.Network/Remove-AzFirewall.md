---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: fce81a5b53383feff4f4b8f5e8993cb1162f920f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091773"
---
# <span data-ttu-id="6c0ea-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ea-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="6c0ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0ea-103">Ta bort en brand vägg.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-103">Remove a Firewall.</span></span>

## <span data-ttu-id="6c0ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c0ea-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c0ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0ea-106">Cmdleten **Remove-AzFirewall** tar bort en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="6c0ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c0ea-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0ea-108">1: skapa och ta bort en brand vägg</span><span class="sxs-lookup"><span data-stu-id="6c0ea-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="6c0ea-109">I det här exemplet skapas en brand vägg och sedan tas den bort.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="6c0ea-110">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="6c0ea-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c0ea-111">PARAMETERS</span></span>

### <span data-ttu-id="6c0ea-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c0ea-112">-AsJob</span></span>
<span data-ttu-id="6c0ea-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6c0ea-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c0ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0ea-114">-DefaultProfile</span></span>
<span data-ttu-id="6c0ea-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c0ea-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6c0ea-116">-Force</span></span>
<span data-ttu-id="6c0ea-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c0ea-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6c0ea-118">-Name</span></span>
<span data-ttu-id="6c0ea-119">Anger namnet på den brand vägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c0ea-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c0ea-120">-PassThru</span></span>
<span data-ttu-id="6c0ea-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c0ea-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c0ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c0ea-124">Anger namnet på den resurs grupp som innehåller den brand vägg som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c0ea-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c0ea-125">-Confirm</span></span>
<span data-ttu-id="6c0ea-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0ea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0ea-127">-WhatIf</span></span>
<span data-ttu-id="6c0ea-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0ea-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0ea-130">CommonParameters</span></span>
<span data-ttu-id="6c0ea-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0ea-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0ea-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0ea-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c0ea-133">INPUTS</span></span>

### <span data-ttu-id="6c0ea-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6c0ea-134">System.String</span></span>

## <span data-ttu-id="6c0ea-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c0ea-135">OUTPUTS</span></span>

### <span data-ttu-id="6c0ea-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c0ea-136">System.Boolean</span></span>

## <span data-ttu-id="6c0ea-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c0ea-137">NOTES</span></span>

## <span data-ttu-id="6c0ea-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c0ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="6c0ea-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ea-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="6c0ea-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ea-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6c0ea-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c0ea-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
