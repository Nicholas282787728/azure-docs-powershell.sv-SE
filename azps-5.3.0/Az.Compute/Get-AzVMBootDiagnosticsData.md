---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526964"
---
# <span data-ttu-id="cbdc3-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cbdc3-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="cbdc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdc3-103">Hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cbdc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbdc3-104">SYNTAX</span></span>

### <span data-ttu-id="cbdc3-105">WindowsParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cbdc3-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbdc3-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="cbdc3-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdc3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbdc3-107">DESCRIPTION</span></span>
<span data-ttu-id="cbdc3-108">Cmdleten **Get-AzVMBootDiagnosticsData** hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cbdc3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbdc3-109">EXAMPLES</span></span>

### <span data-ttu-id="cbdc3-110">Exempel 1: Hämta data från startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="cbdc3-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="cbdc3-111">Det här kommandot får Boot Diagnostics-data för den virtuella datorn med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="cbdc3-112">Denna virtuella dator kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="cbdc3-113">Kommandot lagrar data i angiven lokal sökväg.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="cbdc3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbdc3-114">PARAMETERS</span></span>

### <span data-ttu-id="cbdc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdc3-115">-DefaultProfile</span></span>
<span data-ttu-id="cbdc3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbdc3-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="cbdc3-117">-Linux</span></span>
<span data-ttu-id="cbdc3-118">Anger att den virtuella datorn kör Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc3-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="cbdc3-119">-LocalPath</span></span>
<span data-ttu-id="cbdc3-120">Anger den lokala sökvägen för startdiagnostikens data.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbdc3-121">-Name</span></span>
<span data-ttu-id="cbdc3-122">Anger namnet på den virtuella dator för vilken denna cmdlet hämtar diagnostikdata.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbdc3-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc3-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="cbdc3-125">-Windows</span></span>
<span data-ttu-id="cbdc3-126">Anger att operativ systemet Windows körs på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdc3-127">CommonParameters</span></span>
<span data-ttu-id="cbdc3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbdc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdc3-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbdc3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdc3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbdc3-130">INPUTS</span></span>

### <span data-ttu-id="cbdc3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cbdc3-131">System.String</span></span>

## <span data-ttu-id="cbdc3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbdc3-132">OUTPUTS</span></span>

### <span data-ttu-id="cbdc3-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cbdc3-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cbdc3-134">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="cbdc3-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="cbdc3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbdc3-135">NOTES</span></span>

## <span data-ttu-id="cbdc3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbdc3-136">RELATED LINKS</span></span>

[<span data-ttu-id="cbdc3-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cbdc3-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


