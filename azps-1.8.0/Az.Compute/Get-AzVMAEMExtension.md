---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 8cd67aa715b0092c82a3553158a4736d8f1e850e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917449"
---
# <span data-ttu-id="073b7-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="073b7-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="073b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="073b7-102">SYNOPSIS</span></span>
<span data-ttu-id="073b7-103">Hämtar information om AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="073b7-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="073b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="073b7-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="073b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="073b7-105">DESCRIPTION</span></span>
<span data-ttu-id="073b7-106">Cmdleten **Get-AzVMAEMExtension** hämtar information om tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="073b7-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="073b7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="073b7-107">EXAMPLES</span></span>

### <span data-ttu-id="073b7-108">Exempel 1: skaffa AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="073b7-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="073b7-109">Med det här kommandot får du information om AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="073b7-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="073b7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="073b7-110">PARAMETERS</span></span>

### <span data-ttu-id="073b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073b7-111">-DefaultProfile</span></span>
<span data-ttu-id="073b7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="073b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="073b7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="073b7-113">-Name</span></span>
<span data-ttu-id="073b7-114">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="073b7-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="073b7-115">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="073b7-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="073b7-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="073b7-116">-OSType</span></span>
<span data-ttu-id="073b7-117">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="073b7-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="073b7-118">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="073b7-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="073b7-119">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="073b7-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073b7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073b7-120">-ResourceGroupName</span></span>
<span data-ttu-id="073b7-121">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="073b7-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="073b7-122">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="073b7-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="073b7-123">-Status</span><span class="sxs-lookup"><span data-stu-id="073b7-123">-Status</span></span>
<span data-ttu-id="073b7-124">Anger att denna cmdlet endast får instans vyn för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="073b7-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="073b7-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="073b7-125">-VMName</span></span>
<span data-ttu-id="073b7-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="073b7-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="073b7-127">Denna cmdlet hämtar information om AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="073b7-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="073b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073b7-128">CommonParameters</span></span>
<span data-ttu-id="073b7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073b7-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="073b7-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073b7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="073b7-131">INPUTS</span></span>

### <span data-ttu-id="073b7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="073b7-132">System.String</span></span>

### <span data-ttu-id="073b7-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="073b7-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="073b7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="073b7-134">OUTPUTS</span></span>

### <span data-ttu-id="073b7-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="073b7-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="073b7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="073b7-136">NOTES</span></span>

## <span data-ttu-id="073b7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="073b7-137">RELATED LINKS</span></span>

[<span data-ttu-id="073b7-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="073b7-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="073b7-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="073b7-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="073b7-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="073b7-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


