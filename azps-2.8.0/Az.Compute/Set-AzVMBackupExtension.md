---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: dfcbc8c9b39faae2212bb26098bcfe0f2a966a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744956"
---
# <span data-ttu-id="d64c8-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="d64c8-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="d64c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d64c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d64c8-103">Ställer in egenskaper för säkerhets kopiering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d64c8-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="d64c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d64c8-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d64c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d64c8-105">DESCRIPTION</span></span>

## <span data-ttu-id="d64c8-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d64c8-106">EXAMPLES</span></span>

### <span data-ttu-id="d64c8-107">9.1</span><span class="sxs-lookup"><span data-stu-id="d64c8-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d64c8-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d64c8-108">PARAMETERS</span></span>

### <span data-ttu-id="d64c8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-109">-DefaultProfile</span></span>
<span data-ttu-id="d64c8-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d64c8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64c8-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d64c8-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d64c8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64c8-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d64c8-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d64c8-113">-Tag</span></span>
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

### <span data-ttu-id="d64c8-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="d64c8-114">-VMName</span></span>
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

### <span data-ttu-id="d64c8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64c8-115">CommonParameters</span></span>
<span data-ttu-id="d64c8-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64c8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64c8-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d64c8-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64c8-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d64c8-118">INPUTS</span></span>

### <span data-ttu-id="d64c8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d64c8-119">System.String</span></span>

## <span data-ttu-id="d64c8-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d64c8-120">OUTPUTS</span></span>

### <span data-ttu-id="d64c8-121">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d64c8-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d64c8-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d64c8-122">NOTES</span></span>

## <span data-ttu-id="d64c8-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d64c8-123">RELATED LINKS</span></span>
