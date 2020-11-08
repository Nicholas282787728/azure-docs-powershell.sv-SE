---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089842"
---
# <span data-ttu-id="b3cec-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b3cec-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="b3cec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3cec-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cec-103">Tar bort AEM-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cec-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="b3cec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3cec-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3cec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3cec-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cec-106">Cmdleten **Remove-AzVMAEMExtension** tar bort tillägget Azure Enhanced Monitoring (AEM) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cec-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="b3cec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3cec-107">EXAMPLES</span></span>

### <span data-ttu-id="b3cec-108">Exempel 1: ta bort AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="b3cec-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="b3cec-109">Det här kommandot tar bort AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="b3cec-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="b3cec-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3cec-110">PARAMETERS</span></span>

### <span data-ttu-id="b3cec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cec-111">-DefaultProfile</span></span>
<span data-ttu-id="b3cec-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3cec-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3cec-113">-Name</span></span>
<span data-ttu-id="b3cec-114">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="b3cec-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="b3cec-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b3cec-115">-NoWait</span></span>
<span data-ttu-id="b3cec-116">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="b3cec-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b3cec-117">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b3cec-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cec-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="b3cec-118">-OSType</span></span>
<span data-ttu-id="b3cec-119">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="b3cec-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="b3cec-120">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b3cec-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="b3cec-121">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="b3cec-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3cec-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3cec-123">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cec-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="b3cec-124">Denna cmdlet tar bort AEM-tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b3cec-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="b3cec-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3cec-125">-VMName</span></span>
<span data-ttu-id="b3cec-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b3cec-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b3cec-127">Denna cmdlet tar bort AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b3cec-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3cec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cec-128">CommonParameters</span></span>
<span data-ttu-id="b3cec-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cec-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3cec-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cec-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3cec-131">INPUTS</span></span>

### <span data-ttu-id="b3cec-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3cec-132">System.String</span></span>

## <span data-ttu-id="b3cec-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3cec-133">OUTPUTS</span></span>

### <span data-ttu-id="b3cec-134">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b3cec-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b3cec-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3cec-135">NOTES</span></span>

## <span data-ttu-id="b3cec-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3cec-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3cec-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b3cec-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="b3cec-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b3cec-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="b3cec-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b3cec-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

