---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: ba6d3c19216c8198d4e8cb41fd7fd178cf272ee4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929469"
---
# <span data-ttu-id="3333c-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3333c-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="3333c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3333c-102">SYNOPSIS</span></span>
<span data-ttu-id="3333c-103">Hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3333c-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3333c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3333c-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3333c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3333c-105">DESCRIPTION</span></span>
<span data-ttu-id="3333c-106">Cmdleten **Get-AzureRmVMExtension** hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3333c-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="3333c-107">Ange namnet på ett tillägg som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="3333c-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="3333c-108">Om du bara vill få instans visningen av ett fil namn anger du en status parameter.</span><span class="sxs-lookup"><span data-stu-id="3333c-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="3333c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3333c-109">EXAMPLES</span></span>

### <span data-ttu-id="3333c-110">Exempel 1: Hämta egenskaper för ett tillägg</span><span class="sxs-lookup"><span data-stu-id="3333c-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="3333c-111">Det här kommandot får egenskaper för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3333c-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="3333c-112">Exempel 2: Hämta instans visning av ett tillägg</span><span class="sxs-lookup"><span data-stu-id="3333c-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="3333c-113">Med det här kommandot hämtas instans-vyn för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3333c-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3333c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3333c-114">PARAMETERS</span></span>

### <span data-ttu-id="3333c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3333c-115">-DefaultProfile</span></span>
<span data-ttu-id="3333c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3333c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3333c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3333c-117">-Name</span></span>
<span data-ttu-id="3333c-118">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="3333c-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="3333c-119">Denna cmdlet hämtar egenskaper för tillägget som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3333c-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="3333c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3333c-120">-ResourceGroupName</span></span>
<span data-ttu-id="3333c-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3333c-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3333c-122">-Status</span><span class="sxs-lookup"><span data-stu-id="3333c-122">-Status</span></span>
<span data-ttu-id="3333c-123">Anger att denna cmdlet bara får instans vyn av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="3333c-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="3333c-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="3333c-124">-VMName</span></span>
<span data-ttu-id="3333c-125">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3333c-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3333c-126">Denna cmdlet hämtar egenskaper för ett tillägg från den virtuella dator som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3333c-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3333c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3333c-127">CommonParameters</span></span>
<span data-ttu-id="3333c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3333c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3333c-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3333c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3333c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3333c-130">INPUTS</span></span>

### <span data-ttu-id="3333c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="3333c-131">None</span></span>
<span data-ttu-id="3333c-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3333c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3333c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3333c-133">OUTPUTS</span></span>

### <span data-ttu-id="3333c-134">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3333c-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3333c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3333c-135">NOTES</span></span>

## <span data-ttu-id="3333c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3333c-136">RELATED LINKS</span></span>

[<span data-ttu-id="3333c-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3333c-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="3333c-138">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3333c-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


