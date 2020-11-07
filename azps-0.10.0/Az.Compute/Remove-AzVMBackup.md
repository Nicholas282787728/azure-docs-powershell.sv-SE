---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924977"
---
# <span data-ttu-id="1a63d-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="1a63d-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="1a63d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a63d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a63d-103">Tar bort säkerhets kopian från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1a63d-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="1a63d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a63d-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a63d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a63d-105">DESCRIPTION</span></span>

## <span data-ttu-id="1a63d-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a63d-106">EXAMPLES</span></span>

### <span data-ttu-id="1a63d-107">9.1</span><span class="sxs-lookup"><span data-stu-id="1a63d-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1a63d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a63d-108">PARAMETERS</span></span>

### <span data-ttu-id="1a63d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a63d-109">-DefaultProfile</span></span>
<span data-ttu-id="1a63d-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a63d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a63d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a63d-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1a63d-112">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1a63d-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a63d-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="1a63d-113">-VMName</span></span>
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

### <span data-ttu-id="1a63d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a63d-114">CommonParameters</span></span>
<span data-ttu-id="1a63d-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a63d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a63d-116">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a63d-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a63d-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a63d-117">INPUTS</span></span>

### <span data-ttu-id="1a63d-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a63d-118">None</span></span>
<span data-ttu-id="1a63d-119">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1a63d-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a63d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a63d-120">OUTPUTS</span></span>

### <span data-ttu-id="1a63d-121">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a63d-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1a63d-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a63d-122">NOTES</span></span>

## <span data-ttu-id="1a63d-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a63d-123">RELATED LINKS</span></span>

