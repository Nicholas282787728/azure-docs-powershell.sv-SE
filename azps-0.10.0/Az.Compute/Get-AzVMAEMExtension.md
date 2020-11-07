---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 5efda3a73cc94d2e196b5817d5b3c1e507192da0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925217"
---
# <span data-ttu-id="70bf8-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70bf8-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="70bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="70bf8-103">Hämtar information om AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="70bf8-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="70bf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70bf8-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="70bf8-106">Cmdleten **Get-AzVMAEMExtension** hämtar information om tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="70bf8-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="70bf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="70bf8-108">Exempel 1: skaffa AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="70bf8-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="70bf8-109">Med det här kommandot får du information om AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="70bf8-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="70bf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="70bf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bf8-111">-DefaultProfile</span></span>
<span data-ttu-id="70bf8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70bf8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70bf8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="70bf8-113">-Name</span></span>
<span data-ttu-id="70bf8-114">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="70bf8-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="70bf8-115">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="70bf8-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bf8-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="70bf8-116">-OSType</span></span>
<span data-ttu-id="70bf8-117">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="70bf8-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="70bf8-118">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="70bf8-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="70bf8-119">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="70bf8-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bf8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bf8-120">-ResourceGroupName</span></span>
<span data-ttu-id="70bf8-121">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="70bf8-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="70bf8-122">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="70bf8-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="70bf8-123">-Status</span><span class="sxs-lookup"><span data-stu-id="70bf8-123">-Status</span></span>
<span data-ttu-id="70bf8-124">Anger att denna cmdlet endast får instans vyn för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="70bf8-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="70bf8-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="70bf8-125">-VMName</span></span>
<span data-ttu-id="70bf8-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="70bf8-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="70bf8-127">Denna cmdlet hämtar information om AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="70bf8-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="70bf8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bf8-128">CommonParameters</span></span>
<span data-ttu-id="70bf8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bf8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bf8-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bf8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bf8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70bf8-131">INPUTS</span></span>

### <span data-ttu-id="70bf8-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="70bf8-132">None</span></span>
<span data-ttu-id="70bf8-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="70bf8-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70bf8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70bf8-134">OUTPUTS</span></span>

### <span data-ttu-id="70bf8-135">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="70bf8-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="70bf8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70bf8-136">NOTES</span></span>

## <span data-ttu-id="70bf8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70bf8-137">RELATED LINKS</span></span>

[<span data-ttu-id="70bf8-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70bf8-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="70bf8-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70bf8-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="70bf8-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="70bf8-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


