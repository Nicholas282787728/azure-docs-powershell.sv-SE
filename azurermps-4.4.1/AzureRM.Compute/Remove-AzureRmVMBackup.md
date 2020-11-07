---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: 52abb3af83f7ee0d8724243c917e3aeb58592ac9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756619"
---
# <span data-ttu-id="bff1f-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="bff1f-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="bff1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bff1f-102">SYNOPSIS</span></span>
<span data-ttu-id="bff1f-103">Tar bort säkerhets kopian från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bff1f-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bff1f-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bff1f-105">DESCRIPTION</span></span>

## <span data-ttu-id="bff1f-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bff1f-106">EXAMPLES</span></span>

### <span data-ttu-id="bff1f-107">9.1</span><span class="sxs-lookup"><span data-stu-id="bff1f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="bff1f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bff1f-108">PARAMETERS</span></span>

### <span data-ttu-id="bff1f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff1f-109">-DefaultProfile</span></span>
<span data-ttu-id="bff1f-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bff1f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff1f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff1f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="bff1f-112">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bff1f-112">-Tag</span></span>
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

### <span data-ttu-id="bff1f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="bff1f-113">-VMName</span></span>
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

### <span data-ttu-id="bff1f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff1f-114">CommonParameters</span></span>
<span data-ttu-id="bff1f-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff1f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff1f-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff1f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff1f-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bff1f-117">INPUTS</span></span>

## <span data-ttu-id="bff1f-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bff1f-118">OUTPUTS</span></span>

## <span data-ttu-id="bff1f-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bff1f-119">NOTES</span></span>

## <span data-ttu-id="bff1f-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bff1f-120">RELATED LINKS</span></span>

