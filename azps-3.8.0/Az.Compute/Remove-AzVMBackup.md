---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089839"
---
# <span data-ttu-id="28035-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="28035-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="28035-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28035-102">SYNOPSIS</span></span>
<span data-ttu-id="28035-103">Tar bort säkerhets kopian från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="28035-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="28035-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28035-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28035-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28035-105">DESCRIPTION</span></span>

## <span data-ttu-id="28035-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28035-106">EXAMPLES</span></span>

### <span data-ttu-id="28035-107">9.1</span><span class="sxs-lookup"><span data-stu-id="28035-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="28035-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28035-108">PARAMETERS</span></span>

### <span data-ttu-id="28035-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28035-109">-DefaultProfile</span></span>
<span data-ttu-id="28035-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28035-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28035-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28035-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="28035-112">-Tagg</span><span class="sxs-lookup"><span data-stu-id="28035-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28035-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="28035-113">-VMName</span></span>
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

### <span data-ttu-id="28035-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28035-114">CommonParameters</span></span>
<span data-ttu-id="28035-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28035-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28035-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28035-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28035-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28035-117">INPUTS</span></span>

### <span data-ttu-id="28035-118">System. String</span><span class="sxs-lookup"><span data-stu-id="28035-118">System.String</span></span>

## <span data-ttu-id="28035-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28035-119">OUTPUTS</span></span>

### <span data-ttu-id="28035-120">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="28035-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="28035-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28035-121">NOTES</span></span>

## <span data-ttu-id="28035-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28035-122">RELATED LINKS</span></span>
