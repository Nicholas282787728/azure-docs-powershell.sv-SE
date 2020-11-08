---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925181"
---
# <span data-ttu-id="5c396-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5c396-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="5c396-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c396-102">SYNOPSIS</span></span>
<span data-ttu-id="5c396-103">Hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5c396-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="5c396-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c396-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c396-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c396-105">DESCRIPTION</span></span>
<span data-ttu-id="5c396-106">Cmdleten **Get-AzVMExtension** hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5c396-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="5c396-107">Ange namnet på ett tillägg som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="5c396-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="5c396-108">Om du bara vill få instans visningen av ett fil namn anger du en status parameter.</span><span class="sxs-lookup"><span data-stu-id="5c396-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="5c396-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c396-109">EXAMPLES</span></span>

### <span data-ttu-id="5c396-110">Exempel 1: Hämta egenskaper för ett tillägg</span><span class="sxs-lookup"><span data-stu-id="5c396-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="5c396-111">Det här kommandot får egenskaper för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5c396-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="5c396-112">Exempel 2: Hämta instans visning av ett tillägg</span><span class="sxs-lookup"><span data-stu-id="5c396-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="5c396-113">Med det här kommandot hämtas instans-vyn för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5c396-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="5c396-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c396-114">PARAMETERS</span></span>

### <span data-ttu-id="5c396-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c396-115">-DefaultProfile</span></span>
<span data-ttu-id="5c396-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c396-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c396-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c396-117">-Name</span></span>
<span data-ttu-id="5c396-118">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="5c396-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="5c396-119">Denna cmdlet hämtar egenskaper för tillägget som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5c396-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c396-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c396-120">-ResourceGroupName</span></span>
<span data-ttu-id="5c396-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5c396-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c396-122">-Status</span><span class="sxs-lookup"><span data-stu-id="5c396-122">-Status</span></span>
<span data-ttu-id="5c396-123">Anger att denna cmdlet bara får instans vyn av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="5c396-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c396-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="5c396-124">-VMName</span></span>
<span data-ttu-id="5c396-125">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5c396-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5c396-126">Denna cmdlet hämtar egenskaper för ett tillägg från den virtuella dator som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5c396-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c396-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c396-127">CommonParameters</span></span>
<span data-ttu-id="5c396-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c396-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c396-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c396-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c396-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c396-130">INPUTS</span></span>

### <span data-ttu-id="5c396-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="5c396-131">None</span></span>
<span data-ttu-id="5c396-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5c396-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c396-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c396-133">OUTPUTS</span></span>

### <span data-ttu-id="5c396-134">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5c396-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="5c396-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c396-135">NOTES</span></span>

## <span data-ttu-id="5c396-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c396-136">RELATED LINKS</span></span>

[<span data-ttu-id="5c396-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5c396-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="5c396-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5c396-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

