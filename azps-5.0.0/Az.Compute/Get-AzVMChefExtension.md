---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263348"
---
# <span data-ttu-id="3bc08-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3bc08-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="3bc08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bc08-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc08-103">Hämtar information om en kock-anknytning.</span><span class="sxs-lookup"><span data-stu-id="3bc08-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="3bc08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bc08-104">SYNTAX</span></span>

### <span data-ttu-id="3bc08-105">Linux</span><span class="sxs-lookup"><span data-stu-id="3bc08-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc08-106">Windows</span><span class="sxs-lookup"><span data-stu-id="3bc08-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc08-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bc08-107">DESCRIPTION</span></span>
<span data-ttu-id="3bc08-108">Cmdleten **Get-AzVMChefExtension** hämtar information om en kock-anknytning som är installerad på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3bc08-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="3bc08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bc08-109">EXAMPLES</span></span>

### <span data-ttu-id="3bc08-110">Exempel 1: Hämta information om chefs tillägget för en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="3bc08-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="3bc08-111">Det här kommandot får chefs tillägget från en Windows-dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="3bc08-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="3bc08-112">Exempel 2: Hämta information om chefs tillägget för en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="3bc08-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="3bc08-113">Det här kommandot får chefs tillägget från en virtuell dator med virtuella Linux namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="3bc08-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="3bc08-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bc08-114">PARAMETERS</span></span>

### <span data-ttu-id="3bc08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc08-115">-DefaultProfile</span></span>
<span data-ttu-id="3bc08-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bc08-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3bc08-117">-Linux</span></span>
<span data-ttu-id="3bc08-118">Anger att denna cmdlet fungerar på en virtuell dator med Linux.</span><span class="sxs-lookup"><span data-stu-id="3bc08-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc08-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bc08-119">-Name</span></span>
<span data-ttu-id="3bc08-120">Anger namnet på chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="3bc08-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc08-121">-ResourceGroupName</span></span>
<span data-ttu-id="3bc08-122">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3bc08-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="3bc08-123">-Status</span><span class="sxs-lookup"><span data-stu-id="3bc08-123">-Status</span></span>
<span data-ttu-id="3bc08-124">Anger att denna cmdlet endast får instans vyn av kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="3bc08-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc08-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="3bc08-125">-VMName</span></span>
<span data-ttu-id="3bc08-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3bc08-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc08-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="3bc08-127">-Windows</span></span>
<span data-ttu-id="3bc08-128">Anger att denna cmdlet är för en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="3bc08-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc08-129">CommonParameters</span></span>
<span data-ttu-id="3bc08-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc08-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc08-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bc08-132">INPUTS</span></span>

### <span data-ttu-id="3bc08-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc08-133">System.String</span></span>

### <span data-ttu-id="3bc08-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3bc08-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3bc08-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bc08-135">OUTPUTS</span></span>

### <span data-ttu-id="3bc08-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3bc08-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3bc08-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bc08-137">NOTES</span></span>

## <span data-ttu-id="3bc08-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bc08-138">RELATED LINKS</span></span>

[<span data-ttu-id="3bc08-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3bc08-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="3bc08-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3bc08-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)

