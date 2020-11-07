---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925174"
---
# <span data-ttu-id="55b41-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="55b41-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="55b41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55b41-102">SYNOPSIS</span></span>
<span data-ttu-id="55b41-103">Hämtar statusen för DSC-filtillägg för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="55b41-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="55b41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55b41-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55b41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55b41-105">DESCRIPTION</span></span>
<span data-ttu-id="55b41-106">Cmdleten **Get-AzVMDscExtensionStatus** får statusen för den önskade tilläggs HANTERAREN (DSC) för en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="55b41-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="55b41-107">När en konfiguration används, ger denna cmdlet utdata som är konsekvent med Start-DscConfiguration cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b41-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="55b41-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55b41-108">EXAMPLES</span></span>

### <span data-ttu-id="55b41-109">9.1</span><span class="sxs-lookup"><span data-stu-id="55b41-109">1:</span></span>
```

```

## <span data-ttu-id="55b41-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55b41-110">PARAMETERS</span></span>

### <span data-ttu-id="55b41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b41-111">-DefaultProfile</span></span>
<span data-ttu-id="55b41-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55b41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b41-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="55b41-113">-Name</span></span>
<span data-ttu-id="55b41-114">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="55b41-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="55b41-115">Set-AzVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="55b41-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="55b41-116">Ange endast den här parametern om du har ändrat standard namnet i set cmdlet eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="55b41-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b41-117">-ResourceGroupName</span></span>
<span data-ttu-id="55b41-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="55b41-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="55b41-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="55b41-119">-VMName</span></span>
<span data-ttu-id="55b41-120">Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="55b41-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b41-121">CommonParameters</span></span>
<span data-ttu-id="55b41-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b41-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b41-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b41-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55b41-124">INPUTS</span></span>

### <span data-ttu-id="55b41-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="55b41-125">None</span></span>
<span data-ttu-id="55b41-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="55b41-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55b41-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55b41-127">OUTPUTS</span></span>

### <span data-ttu-id="55b41-128">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="55b41-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="55b41-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55b41-129">NOTES</span></span>

## <span data-ttu-id="55b41-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55b41-130">RELATED LINKS</span></span>

[<span data-ttu-id="55b41-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="55b41-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


