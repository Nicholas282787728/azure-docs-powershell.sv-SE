---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930645"
---
# <span data-ttu-id="c0e45-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0e45-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="c0e45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0e45-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e45-103">Tar bort AEM-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c0e45-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0e45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0e45-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0e45-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0e45-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e45-106">Cmdleten **Remove-AzureRmVMAEMExtension** tar bort tillägget Azure Enhanced Monitoring (AEM) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c0e45-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="c0e45-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0e45-107">EXAMPLES</span></span>

### <span data-ttu-id="c0e45-108">Exempel 1: ta bort AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="c0e45-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c0e45-109">Det här kommandot tar bort AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="c0e45-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c0e45-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0e45-110">PARAMETERS</span></span>

### <span data-ttu-id="c0e45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e45-111">-DefaultProfile</span></span>
<span data-ttu-id="c0e45-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e45-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e45-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0e45-113">-Name</span></span>
<span data-ttu-id="c0e45-114">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="c0e45-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="c0e45-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="c0e45-115">-OSType</span></span>
<span data-ttu-id="c0e45-116">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="c0e45-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c0e45-117">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c0e45-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c0e45-118">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="c0e45-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="c0e45-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e45-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0e45-120">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c0e45-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="c0e45-121">Denna cmdlet tar bort AEM-tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c0e45-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="c0e45-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0e45-122">-VMName</span></span>
<span data-ttu-id="c0e45-123">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c0e45-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c0e45-124">Denna cmdlet tar bort AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c0e45-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0e45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e45-125">CommonParameters</span></span>
<span data-ttu-id="c0e45-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e45-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e45-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e45-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0e45-128">INPUTS</span></span>

### <span data-ttu-id="c0e45-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="c0e45-129">None</span></span>
<span data-ttu-id="c0e45-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c0e45-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0e45-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0e45-131">OUTPUTS</span></span>

### <span data-ttu-id="c0e45-132">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c0e45-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c0e45-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0e45-133">NOTES</span></span>

## <span data-ttu-id="c0e45-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0e45-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0e45-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0e45-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c0e45-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0e45-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c0e45-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c0e45-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


