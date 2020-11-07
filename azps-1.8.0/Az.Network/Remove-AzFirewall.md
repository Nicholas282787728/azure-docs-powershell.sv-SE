---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747892"
---
# <span data-ttu-id="06904-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06904-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="06904-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06904-102">SYNOPSIS</span></span>
<span data-ttu-id="06904-103">Ta bort en brand vägg.</span><span class="sxs-lookup"><span data-stu-id="06904-103">Remove a Firewall.</span></span>

## <span data-ttu-id="06904-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06904-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06904-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06904-105">DESCRIPTION</span></span>
<span data-ttu-id="06904-106">Cmdleten **Remove-AzFirewall** tar bort en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="06904-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="06904-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06904-107">EXAMPLES</span></span>

### <span data-ttu-id="06904-108">1: skapa och ta bort en brand vägg</span><span class="sxs-lookup"><span data-stu-id="06904-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="06904-109">I det här exemplet skapas en brand vägg och sedan tas den bort.</span><span class="sxs-lookup"><span data-stu-id="06904-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="06904-110">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="06904-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="06904-111">2: frigör brand väggen och ta sedan bort brand väggen</span><span class="sxs-lookup"><span data-stu-id="06904-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="06904-112">Det här exemplet hämtar en brand vägg, avsätter brand väggen och tar sedan bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="06904-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="06904-113">Kommandot frigör tar bort den aktiva tjänsten men bevarar brand väggens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="06904-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="06904-114">Om användaren vill starta tjänsten igen ska metoden allocate anropas i brand väggen.</span><span class="sxs-lookup"><span data-stu-id="06904-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="06904-115">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="06904-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="06904-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06904-116">PARAMETERS</span></span>

### <span data-ttu-id="06904-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06904-117">-AsJob</span></span>
<span data-ttu-id="06904-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06904-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06904-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06904-119">-DefaultProfile</span></span>
<span data-ttu-id="06904-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06904-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06904-121">-Force</span><span class="sxs-lookup"><span data-stu-id="06904-121">-Force</span></span>
<span data-ttu-id="06904-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="06904-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06904-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="06904-123">-Name</span></span>
<span data-ttu-id="06904-124">Anger namnet på den brand vägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="06904-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="06904-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06904-125">-PassThru</span></span>
<span data-ttu-id="06904-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="06904-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06904-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="06904-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06904-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06904-128">-ResourceGroupName</span></span>
<span data-ttu-id="06904-129">Anger namnet på den resurs grupp som innehåller den brand vägg som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06904-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="06904-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06904-130">-Confirm</span></span>
<span data-ttu-id="06904-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06904-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06904-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06904-132">-WhatIf</span></span>
<span data-ttu-id="06904-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06904-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06904-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06904-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06904-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06904-135">CommonParameters</span></span>
<span data-ttu-id="06904-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06904-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06904-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06904-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06904-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06904-138">INPUTS</span></span>

### <span data-ttu-id="06904-139">System. String</span><span class="sxs-lookup"><span data-stu-id="06904-139">System.String</span></span>

## <span data-ttu-id="06904-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06904-140">OUTPUTS</span></span>

### <span data-ttu-id="06904-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06904-141">System.Boolean</span></span>

## <span data-ttu-id="06904-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06904-142">NOTES</span></span>

## <span data-ttu-id="06904-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06904-143">RELATED LINKS</span></span>

[<span data-ttu-id="06904-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06904-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="06904-145">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06904-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="06904-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06904-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
