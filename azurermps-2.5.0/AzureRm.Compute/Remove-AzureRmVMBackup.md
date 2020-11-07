---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930634"
---
# <span data-ttu-id="9e989-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="9e989-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="9e989-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e989-102">SYNOPSIS</span></span>
<span data-ttu-id="9e989-103">Tar bort säkerhets kopian från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9e989-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e989-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e989-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e989-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e989-105">DESCRIPTION</span></span>

## <span data-ttu-id="9e989-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e989-106">EXAMPLES</span></span>

### <span data-ttu-id="9e989-107">9.1</span><span class="sxs-lookup"><span data-stu-id="9e989-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9e989-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e989-108">PARAMETERS</span></span>

### <span data-ttu-id="9e989-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e989-109">-DefaultProfile</span></span>
<span data-ttu-id="9e989-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e989-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e989-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e989-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9e989-112">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9e989-112">-Tag</span></span>
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

### <span data-ttu-id="9e989-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e989-113">-VMName</span></span>
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

### <span data-ttu-id="9e989-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e989-114">CommonParameters</span></span>
<span data-ttu-id="9e989-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e989-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e989-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e989-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e989-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e989-117">INPUTS</span></span>

### <span data-ttu-id="9e989-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e989-118">None</span></span>
<span data-ttu-id="9e989-119">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9e989-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e989-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e989-120">OUTPUTS</span></span>

### <span data-ttu-id="9e989-121">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9e989-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e989-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e989-122">NOTES</span></span>

## <span data-ttu-id="9e989-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e989-123">RELATED LINKS</span></span>

