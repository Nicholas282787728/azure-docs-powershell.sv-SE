---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928914"
---
# <span data-ttu-id="803da-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="803da-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="803da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="803da-102">SYNOPSIS</span></span>
<span data-ttu-id="803da-103">Hämtar statusen för DSC-filtillägg för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="803da-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="803da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="803da-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="803da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="803da-105">DESCRIPTION</span></span>
<span data-ttu-id="803da-106">Cmdleten **Get-AzureRmVMDscExtensionStatus** får statusen för den önskade tilläggs HANTERAREN (DSC) för en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="803da-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="803da-107">När en konfiguration används, ger denna cmdlet utdata som är konsekvent med Start-DscConfiguration cmdlet.</span><span class="sxs-lookup"><span data-stu-id="803da-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="803da-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="803da-108">EXAMPLES</span></span>

### <span data-ttu-id="803da-109">9.1</span><span class="sxs-lookup"><span data-stu-id="803da-109">1:</span></span>
```

```

## <span data-ttu-id="803da-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="803da-110">PARAMETERS</span></span>

### <span data-ttu-id="803da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803da-111">-DefaultProfile</span></span>
<span data-ttu-id="803da-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="803da-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="803da-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="803da-113">-Name</span></span>
<span data-ttu-id="803da-114">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="803da-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="803da-115">Set-AzureRmVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="803da-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="803da-116">Ange endast den här parametern om du har ändrat standard namnet i set cmdlet eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="803da-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="803da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="803da-117">-ResourceGroupName</span></span>
<span data-ttu-id="803da-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="803da-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="803da-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="803da-119">-VMName</span></span>
<span data-ttu-id="803da-120">Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="803da-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="803da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803da-121">CommonParameters</span></span>
<span data-ttu-id="803da-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803da-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="803da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803da-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="803da-124">INPUTS</span></span>

### <span data-ttu-id="803da-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="803da-125">None</span></span>
<span data-ttu-id="803da-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="803da-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="803da-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="803da-127">OUTPUTS</span></span>

### <span data-ttu-id="803da-128">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="803da-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="803da-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="803da-129">NOTES</span></span>

## <span data-ttu-id="803da-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="803da-130">RELATED LINKS</span></span>

[<span data-ttu-id="803da-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="803da-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


