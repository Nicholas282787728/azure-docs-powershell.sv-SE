---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: cb28249d5c32119d187becd8b07f2137f3f312d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755347"
---
# <span data-ttu-id="55041-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="55041-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="55041-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55041-102">SYNOPSIS</span></span>
<span data-ttu-id="55041-103">Tar bort säkerhets kopian från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="55041-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55041-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55041-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55041-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55041-105">DESCRIPTION</span></span>

## <span data-ttu-id="55041-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55041-106">EXAMPLES</span></span>

### <span data-ttu-id="55041-107">9.1</span><span class="sxs-lookup"><span data-stu-id="55041-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="55041-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55041-108">PARAMETERS</span></span>

### <span data-ttu-id="55041-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55041-109">-DefaultProfile</span></span>
<span data-ttu-id="55041-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55041-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55041-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55041-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="55041-112">-Tagg</span><span class="sxs-lookup"><span data-stu-id="55041-112">-Tag</span></span>
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

### <span data-ttu-id="55041-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="55041-113">-VMName</span></span>
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

### <span data-ttu-id="55041-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55041-114">CommonParameters</span></span>
<span data-ttu-id="55041-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55041-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55041-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55041-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55041-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55041-117">INPUTS</span></span>

### <span data-ttu-id="55041-118">System. String</span><span class="sxs-lookup"><span data-stu-id="55041-118">System.String</span></span>

## <span data-ttu-id="55041-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55041-119">OUTPUTS</span></span>

### <span data-ttu-id="55041-120">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="55041-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="55041-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55041-121">NOTES</span></span>

## <span data-ttu-id="55041-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55041-122">RELATED LINKS</span></span>
