---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 6a47e5a248c5de3c2dd87af67393f60d215e44c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573706"
---
# <span data-ttu-id="05123-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05123-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="05123-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05123-102">SYNOPSIS</span></span>
<span data-ttu-id="05123-103">Tar bort tillägget diagnostik från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="05123-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05123-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05123-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05123-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05123-105">DESCRIPTION</span></span>
<span data-ttu-id="05123-106">Cmdleten **Remove-AzureRmVMDiagnosticsExtension** tar bort ett Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="05123-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="05123-107">Du måste skicka utdata från denna cmdlet till Update-AzureRmVM cmdlet för att implementera ändringarna.</span><span class="sxs-lookup"><span data-stu-id="05123-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="05123-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05123-108">EXAMPLES</span></span>

### <span data-ttu-id="05123-109">Exempel 1: ta bort tillägget diagnostik från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="05123-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="05123-110">Det här kommandot tar bort tillägget från en virtuell dator med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="05123-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="05123-111">Kommandot skickar resultatet till Update-AzureRmVM cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="05123-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="05123-112">Det kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="05123-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="05123-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05123-113">PARAMETERS</span></span>

### <span data-ttu-id="05123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05123-114">-DefaultProfile</span></span>
<span data-ttu-id="05123-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05123-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05123-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="05123-116">-Name</span></span>
<span data-ttu-id="05123-117">Anger namnet på den diagnostiska anknytning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="05123-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05123-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05123-118">-ResourceGroupName</span></span>
<span data-ttu-id="05123-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="05123-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="05123-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="05123-120">-VMName</span></span>
<span data-ttu-id="05123-121">Anger namnet på den virtuella dator som cmdleten tar bort ett diagnostiktest från.</span><span class="sxs-lookup"><span data-stu-id="05123-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="05123-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05123-122">CommonParameters</span></span>
<span data-ttu-id="05123-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05123-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05123-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05123-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05123-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05123-125">INPUTS</span></span>

## <span data-ttu-id="05123-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05123-126">OUTPUTS</span></span>

## <span data-ttu-id="05123-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05123-127">NOTES</span></span>

## <span data-ttu-id="05123-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05123-128">RELATED LINKS</span></span>

[<span data-ttu-id="05123-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05123-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="05123-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05123-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="05123-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05123-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


