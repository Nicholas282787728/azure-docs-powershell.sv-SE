---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260810"
---
# <span data-ttu-id="9c7c0-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="9c7c0-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="9c7c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7c0-103">Ställer in egenskaper för säkerhets kopiering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9c7c0-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="9c7c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c7c0-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c7c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c7c0-105">DESCRIPTION</span></span>

## <span data-ttu-id="9c7c0-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c7c0-106">EXAMPLES</span></span>

### <span data-ttu-id="9c7c0-107">9.1</span><span class="sxs-lookup"><span data-stu-id="9c7c0-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9c7c0-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c7c0-108">PARAMETERS</span></span>

### <span data-ttu-id="9c7c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7c0-109">-DefaultProfile</span></span>
<span data-ttu-id="9c7c0-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7c0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7c0-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c7c0-111">-Name</span></span>
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

### <span data-ttu-id="9c7c0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7c0-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9c7c0-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9c7c0-113">-Tag</span></span>
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

### <span data-ttu-id="9c7c0-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c7c0-114">-VMName</span></span>
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

### <span data-ttu-id="9c7c0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7c0-115">CommonParameters</span></span>
<span data-ttu-id="9c7c0-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c7c0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7c0-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c7c0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7c0-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c7c0-118">INPUTS</span></span>

### <span data-ttu-id="9c7c0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7c0-119">System.String</span></span>

## <span data-ttu-id="9c7c0-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c7c0-120">OUTPUTS</span></span>

### <span data-ttu-id="9c7c0-121">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c7c0-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c7c0-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c7c0-122">NOTES</span></span>

## <span data-ttu-id="9c7c0-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c7c0-123">RELATED LINKS</span></span>
