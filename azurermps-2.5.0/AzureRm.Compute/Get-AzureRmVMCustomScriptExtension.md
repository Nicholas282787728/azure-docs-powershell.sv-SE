---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931518"
---
# <span data-ttu-id="acc58-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="acc58-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="acc58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acc58-102">SYNOPSIS</span></span>
<span data-ttu-id="acc58-103">Hämtar information om ett anpassat skript tillägg.</span><span class="sxs-lookup"><span data-stu-id="acc58-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acc58-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acc58-105">DESCRIPTION</span></span>
<span data-ttu-id="acc58-106">Cmdleten **Get-AzureRmVMCustomScriptExtension** hämtar information om ett anpassat namn för en virtuell dator för skript för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="acc58-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="acc58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acc58-107">EXAMPLES</span></span>

### <span data-ttu-id="acc58-108">Exempel 1: Hämta ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="acc58-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="acc58-109">Det här kommandot hämtar det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="acc58-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="acc58-110">Exempel 2: Hämta instans visningen av ett anpassat skript tillägg</span><span class="sxs-lookup"><span data-stu-id="acc58-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="acc58-111">Det här kommandot hämtar instans vyn för det anpassade skript tillägget med namnet ContosoCustomScript för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="acc58-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="acc58-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acc58-112">PARAMETERS</span></span>

### <span data-ttu-id="acc58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc58-113">-DefaultProfile</span></span>
<span data-ttu-id="acc58-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acc58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc58-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="acc58-115">-Name</span></span>
<span data-ttu-id="acc58-116">Anger namnet på det anpassade skript tillägget som innehåller information om den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acc58-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="acc58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc58-117">-ResourceGroupName</span></span>
<span data-ttu-id="acc58-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="acc58-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="acc58-119">-Status</span><span class="sxs-lookup"><span data-stu-id="acc58-119">-Status</span></span>
<span data-ttu-id="acc58-120">Anger att denna cmdlet får instans vyn för det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="acc58-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="acc58-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="acc58-121">-VMName</span></span>
<span data-ttu-id="acc58-122">Anger namnet på en virtuell dator för vilken denna cmdlet får det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="acc58-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="acc58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc58-123">CommonParameters</span></span>
<span data-ttu-id="acc58-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc58-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc58-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc58-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acc58-126">INPUTS</span></span>

### <span data-ttu-id="acc58-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="acc58-127">None</span></span>
<span data-ttu-id="acc58-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="acc58-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acc58-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acc58-129">OUTPUTS</span></span>

### <span data-ttu-id="acc58-130">Microsoft. Azure. commands. Compute. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="acc58-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="acc58-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acc58-131">NOTES</span></span>

## <span data-ttu-id="acc58-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acc58-132">RELATED LINKS</span></span>

[<span data-ttu-id="acc58-133">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="acc58-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="acc58-134">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="acc58-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="acc58-135">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="acc58-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

