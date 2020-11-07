---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930317"
---
# <span data-ttu-id="03211-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="03211-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="03211-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03211-102">SYNOPSIS</span></span>
<span data-ttu-id="03211-103">Tar bort (a) hemliga (a) hemligheter från ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="03211-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03211-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03211-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03211-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03211-105">DESCRIPTION</span></span>
<span data-ttu-id="03211-106">Remove-AzureRmVMSecret-cmdleten tar bort (a) hemligheter från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="03211-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="03211-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03211-107">EXAMPLES</span></span>

### <span data-ttu-id="03211-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03211-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="03211-109">Tar bort alla hemligheter från en virtuell dator "VM1" i resurs gruppen "RG1" och uppdaterar den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="03211-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="03211-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03211-110">PARAMETERS</span></span>

### <span data-ttu-id="03211-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03211-111">-DefaultProfile</span></span>
<span data-ttu-id="03211-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03211-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03211-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="03211-113">-SourceVaultId</span></span>
<span data-ttu-id="03211-114">Anger en matris med käll valv-ID: n som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="03211-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03211-115">-VM</span><span class="sxs-lookup"><span data-stu-id="03211-115">-VM</span></span>
<span data-ttu-id="03211-116">Anger den virtuella dator från vilken denna cmdlet tar bort (a) hemlighet (s).</span><span class="sxs-lookup"><span data-stu-id="03211-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="03211-117">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="03211-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03211-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03211-118">-Confirm</span></span>
<span data-ttu-id="03211-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03211-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03211-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03211-120">-WhatIf</span></span>
<span data-ttu-id="03211-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03211-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03211-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03211-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03211-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03211-123">CommonParameters</span></span>
<span data-ttu-id="03211-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03211-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03211-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03211-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03211-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03211-126">INPUTS</span></span>

### <span data-ttu-id="03211-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="03211-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="03211-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03211-128">OUTPUTS</span></span>

### <span data-ttu-id="03211-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="03211-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="03211-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03211-130">NOTES</span></span>

## <span data-ttu-id="03211-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03211-131">RELATED LINKS</span></span>

