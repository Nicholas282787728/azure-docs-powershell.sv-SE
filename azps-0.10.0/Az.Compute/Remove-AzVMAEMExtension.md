---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924997"
---
# <span data-ttu-id="385a1-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="385a1-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="385a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="385a1-102">SYNOPSIS</span></span>
<span data-ttu-id="385a1-103">Tar bort AEM-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="385a1-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="385a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="385a1-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="385a1-105">DESCRIPTION</span></span>
<span data-ttu-id="385a1-106">Cmdleten **Remove-AzVMAEMExtension** tar bort tillägget Azure Enhanced Monitoring (AEM) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="385a1-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="385a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="385a1-107">EXAMPLES</span></span>

### <span data-ttu-id="385a1-108">Exempel 1: ta bort AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="385a1-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="385a1-109">Det här kommandot tar bort AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="385a1-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="385a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="385a1-110">PARAMETERS</span></span>

### <span data-ttu-id="385a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385a1-111">-DefaultProfile</span></span>
<span data-ttu-id="385a1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="385a1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385a1-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="385a1-113">-Name</span></span>
<span data-ttu-id="385a1-114">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="385a1-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="385a1-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="385a1-115">-OSType</span></span>
<span data-ttu-id="385a1-116">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="385a1-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="385a1-117">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="385a1-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="385a1-118">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="385a1-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="385a1-120">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="385a1-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="385a1-121">Denna cmdlet tar bort AEM-tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="385a1-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="385a1-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="385a1-122">-VMName</span></span>
<span data-ttu-id="385a1-123">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="385a1-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="385a1-124">Denna cmdlet tar bort AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="385a1-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="385a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385a1-125">CommonParameters</span></span>
<span data-ttu-id="385a1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385a1-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385a1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385a1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="385a1-128">INPUTS</span></span>

### <span data-ttu-id="385a1-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="385a1-129">None</span></span>
<span data-ttu-id="385a1-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="385a1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="385a1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="385a1-131">OUTPUTS</span></span>

### <span data-ttu-id="385a1-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="385a1-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="385a1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="385a1-133">NOTES</span></span>

## <span data-ttu-id="385a1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="385a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="385a1-135">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="385a1-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="385a1-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="385a1-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="385a1-137">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="385a1-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


