---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573671"
---
# <span data-ttu-id="499ed-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="499ed-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="499ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="499ed-102">SYNOPSIS</span></span>
<span data-ttu-id="499ed-103">Ställer in egenskaper för säkerhets kopiering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="499ed-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="499ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="499ed-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="499ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="499ed-105">DESCRIPTION</span></span>

## <span data-ttu-id="499ed-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="499ed-106">EXAMPLES</span></span>

### <span data-ttu-id="499ed-107">9.1</span><span class="sxs-lookup"><span data-stu-id="499ed-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="499ed-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="499ed-108">PARAMETERS</span></span>

### <span data-ttu-id="499ed-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499ed-109">-DefaultProfile</span></span>
<span data-ttu-id="499ed-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="499ed-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="499ed-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="499ed-111">-Name</span></span>
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

### <span data-ttu-id="499ed-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499ed-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="499ed-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="499ed-113">-Tag</span></span>
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

### <span data-ttu-id="499ed-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="499ed-114">-VMName</span></span>
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

### <span data-ttu-id="499ed-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499ed-115">CommonParameters</span></span>
<span data-ttu-id="499ed-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499ed-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499ed-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="499ed-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499ed-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="499ed-118">INPUTS</span></span>

## <span data-ttu-id="499ed-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="499ed-119">OUTPUTS</span></span>

## <span data-ttu-id="499ed-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="499ed-120">NOTES</span></span>

## <span data-ttu-id="499ed-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="499ed-121">RELATED LINKS</span></span>

