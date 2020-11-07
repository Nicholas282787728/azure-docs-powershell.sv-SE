---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924826"
---
# <span data-ttu-id="84492-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="84492-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="84492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84492-102">SYNOPSIS</span></span>
<span data-ttu-id="84492-103">Ställer in egenskaper för säkerhets kopiering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="84492-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="84492-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84492-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84492-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84492-105">DESCRIPTION</span></span>

## <span data-ttu-id="84492-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84492-106">EXAMPLES</span></span>

### <span data-ttu-id="84492-107">9.1</span><span class="sxs-lookup"><span data-stu-id="84492-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="84492-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84492-108">PARAMETERS</span></span>

### <span data-ttu-id="84492-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84492-109">-DefaultProfile</span></span>
<span data-ttu-id="84492-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84492-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84492-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="84492-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84492-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84492-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="84492-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="84492-113">-Tag</span></span>
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

### <span data-ttu-id="84492-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="84492-114">-VMName</span></span>
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

### <span data-ttu-id="84492-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84492-115">CommonParameters</span></span>
<span data-ttu-id="84492-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84492-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84492-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84492-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84492-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84492-118">INPUTS</span></span>

### <span data-ttu-id="84492-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="84492-119">None</span></span>
<span data-ttu-id="84492-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="84492-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84492-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84492-121">OUTPUTS</span></span>

### <span data-ttu-id="84492-122">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84492-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="84492-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84492-123">NOTES</span></span>

## <span data-ttu-id="84492-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84492-124">RELATED LINKS</span></span>

