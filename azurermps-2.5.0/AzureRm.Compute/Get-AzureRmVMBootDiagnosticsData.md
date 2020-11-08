---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929474"
---
# <span data-ttu-id="cfa9c-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cfa9c-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="cfa9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfa9c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa9c-103">Hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfa9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfa9c-104">SYNTAX</span></span>

### <span data-ttu-id="cfa9c-105">WindowsParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cfa9c-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfa9c-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="cfa9c-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa9c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfa9c-107">DESCRIPTION</span></span>
<span data-ttu-id="cfa9c-108">Cmdleten **Get-AzureRmVMBootDiagnosticsData** hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cfa9c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfa9c-109">EXAMPLES</span></span>

### <span data-ttu-id="cfa9c-110">Exempel 1: Hämta data från startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="cfa9c-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="cfa9c-111">Det här kommandot får Boot Diagnostics-data för den virtuella datorn med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="cfa9c-112">Denna virtuella dator kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="cfa9c-113">Kommandot lagrar data i angiven lokal sökväg.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="cfa9c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfa9c-114">PARAMETERS</span></span>

### <span data-ttu-id="cfa9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa9c-115">-DefaultProfile</span></span>
<span data-ttu-id="cfa9c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa9c-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="cfa9c-117">-Linux</span></span>
<span data-ttu-id="cfa9c-118">Anger att den virtuella datorn kör Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9c-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="cfa9c-119">-LocalPath</span></span>
<span data-ttu-id="cfa9c-120">Anger den lokala sökvägen för startdiagnostikens data.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfa9c-121">-Name</span></span>
<span data-ttu-id="cfa9c-122">Anger namnet på den virtuella dator för vilken denna cmdlet hämtar diagnostikdata.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa9c-123">-ResourceGroupName</span></span>
<span data-ttu-id="cfa9c-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cfa9c-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="cfa9c-125">-Windows</span></span>
<span data-ttu-id="cfa9c-126">Anger att operativ systemet Windows körs på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa9c-127">CommonParameters</span></span>
<span data-ttu-id="cfa9c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa9c-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa9c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa9c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfa9c-130">INPUTS</span></span>

### <span data-ttu-id="cfa9c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="cfa9c-131">None</span></span>
<span data-ttu-id="cfa9c-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cfa9c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfa9c-133">OUTPUTS</span></span>

### <span data-ttu-id="cfa9c-134">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cfa9c-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cfa9c-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="cfa9c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="cfa9c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfa9c-136">NOTES</span></span>

## <span data-ttu-id="cfa9c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfa9c-137">RELATED LINKS</span></span>

[<span data-ttu-id="cfa9c-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cfa9c-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)

