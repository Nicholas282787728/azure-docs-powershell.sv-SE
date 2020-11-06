---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576176"
---
# <span data-ttu-id="9eccb-101">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9eccb-101">Remove-AzureRmFirewall</span></span>

## <span data-ttu-id="9eccb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eccb-102">SYNOPSIS</span></span>
<span data-ttu-id="9eccb-103">Ta bort en brand vägg.</span><span class="sxs-lookup"><span data-stu-id="9eccb-103">Remove a Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eccb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eccb-104">SYNTAX</span></span>

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eccb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eccb-105">DESCRIPTION</span></span>
<span data-ttu-id="9eccb-106">Cmdleten **Remove-AzureRmFirewall** tar bort en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="9eccb-106">The **Remove-AzureRmFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="9eccb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eccb-107">EXAMPLES</span></span>

### <span data-ttu-id="9eccb-108">1: skapa och ta bort en brand vägg</span><span class="sxs-lookup"><span data-stu-id="9eccb-108">1: Create and delete a Firewall</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9eccb-109">I det här exemplet skapas en brand vägg och sedan tas den bort.</span><span class="sxs-lookup"><span data-stu-id="9eccb-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="9eccb-110">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="9eccb-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="9eccb-111">2: frigör brand väggen och ta sedan bort brand väggen</span><span class="sxs-lookup"><span data-stu-id="9eccb-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9eccb-112">Det här exemplet hämtar en brand vägg, avsätter brand väggen och tar sedan bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="9eccb-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="9eccb-113">Kommandot frigör tar bort den aktiva tjänsten men bevarar brand väggens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9eccb-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="9eccb-114">Om användaren vill starta tjänsten igen ska metoden allocate anropas i brand väggen.</span><span class="sxs-lookup"><span data-stu-id="9eccb-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="9eccb-115">Använd flaggan-Force för att utelämna uppmaningen när du tar bort brand väggen.</span><span class="sxs-lookup"><span data-stu-id="9eccb-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="9eccb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eccb-116">PARAMETERS</span></span>

### <span data-ttu-id="9eccb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eccb-117">-AsJob</span></span>
<span data-ttu-id="9eccb-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9eccb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eccb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eccb-119">-DefaultProfile</span></span>
<span data-ttu-id="9eccb-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9eccb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eccb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9eccb-121">-Force</span></span>
<span data-ttu-id="9eccb-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9eccb-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9eccb-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eccb-123">-Name</span></span>
<span data-ttu-id="9eccb-124">Anger namnet på den brand vägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9eccb-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9eccb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eccb-125">-PassThru</span></span>
<span data-ttu-id="9eccb-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9eccb-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eccb-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9eccb-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eccb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eccb-128">-ResourceGroupName</span></span>
<span data-ttu-id="9eccb-129">Anger namnet på den resurs grupp som innehåller den brand vägg som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eccb-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9eccb-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9eccb-130">-Confirm</span></span>
<span data-ttu-id="9eccb-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9eccb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eccb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eccb-132">-WhatIf</span></span>
<span data-ttu-id="9eccb-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9eccb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eccb-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9eccb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eccb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eccb-135">CommonParameters</span></span>
<span data-ttu-id="9eccb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eccb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eccb-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eccb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eccb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eccb-138">INPUTS</span></span>

### <span data-ttu-id="9eccb-139">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9eccb-139">PSAzureFirewall</span></span>
<span data-ttu-id="9eccb-140">Skriv ' PSAzureFirewall ' är accepterat från pipeline</span><span class="sxs-lookup"><span data-stu-id="9eccb-140">Type 'PSAzureFirewall' is accepted from the pipeline</span></span>

## <span data-ttu-id="9eccb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eccb-141">OUTPUTS</span></span>

## <span data-ttu-id="9eccb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eccb-142">NOTES</span></span>

## <span data-ttu-id="9eccb-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eccb-143">RELATED LINKS</span></span>

[<span data-ttu-id="9eccb-144">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9eccb-144">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="9eccb-145">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9eccb-145">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="9eccb-146">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9eccb-146">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
