---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401451"
---
# <span data-ttu-id="cadf6-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cadf6-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="cadf6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cadf6-102">SYNOPSIS</span></span>
<span data-ttu-id="cadf6-103">Ta bort en brand vägg.</span><span class="sxs-lookup"><span data-stu-id="cadf6-103">Remove a Firewall.</span></span>

## <span data-ttu-id="cadf6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cadf6-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadf6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cadf6-105">DESCRIPTION</span></span>
<span data-ttu-id="cadf6-106">Cmdleten **Remove-AzFirewall** tar bort en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="cadf6-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="cadf6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cadf6-107">EXAMPLES</span></span>

### <span data-ttu-id="cadf6-108">Exempel 1: skapa och ta bort en brand vägg</span><span class="sxs-lookup"><span data-stu-id="cadf6-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="cadf6-109">I det här exemplet skapas en brand vägg och sedan tas den bort.</span><span class="sxs-lookup"><span data-stu-id="cadf6-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="cadf6-110">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="cadf6-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="cadf6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cadf6-111">PARAMETERS</span></span>

### <span data-ttu-id="cadf6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cadf6-112">-AsJob</span></span>
<span data-ttu-id="cadf6-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cadf6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cadf6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadf6-114">-DefaultProfile</span></span>
<span data-ttu-id="cadf6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cadf6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cadf6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cadf6-116">-Force</span></span>
<span data-ttu-id="cadf6-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cadf6-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cadf6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="cadf6-118">-Name</span></span>
<span data-ttu-id="cadf6-119">Anger namnet på den brand vägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cadf6-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cadf6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cadf6-120">-PassThru</span></span>
<span data-ttu-id="cadf6-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="cadf6-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cadf6-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cadf6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cadf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="cadf6-124">Anger namnet på den resurs grupp som innehåller den brand vägg som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cadf6-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cadf6-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cadf6-125">-Confirm</span></span>
<span data-ttu-id="cadf6-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cadf6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadf6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadf6-127">-WhatIf</span></span>
<span data-ttu-id="cadf6-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cadf6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadf6-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cadf6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadf6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadf6-130">CommonParameters</span></span>
<span data-ttu-id="cadf6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadf6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadf6-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadf6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadf6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cadf6-133">INPUTS</span></span>

### <span data-ttu-id="cadf6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cadf6-134">System.String</span></span>

## <span data-ttu-id="cadf6-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cadf6-135">OUTPUTS</span></span>

### <span data-ttu-id="cadf6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cadf6-136">System.Boolean</span></span>

## <span data-ttu-id="cadf6-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cadf6-137">NOTES</span></span>

## <span data-ttu-id="cadf6-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cadf6-138">RELATED LINKS</span></span>

[<span data-ttu-id="cadf6-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cadf6-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="cadf6-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cadf6-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="cadf6-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cadf6-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
