---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930266"
---
# <span data-ttu-id="d75b7-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="d75b7-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="d75b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d75b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d75b7-103">Ställer in egenskaper för säkerhets kopiering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d75b7-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d75b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d75b7-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d75b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d75b7-105">DESCRIPTION</span></span>

## <span data-ttu-id="d75b7-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d75b7-106">EXAMPLES</span></span>

### <span data-ttu-id="d75b7-107">9.1</span><span class="sxs-lookup"><span data-stu-id="d75b7-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d75b7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d75b7-108">PARAMETERS</span></span>

### <span data-ttu-id="d75b7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75b7-109">-DefaultProfile</span></span>
<span data-ttu-id="d75b7-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d75b7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d75b7-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d75b7-111">-Name</span></span>
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

### <span data-ttu-id="d75b7-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75b7-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d75b7-113">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d75b7-113">-Tag</span></span>
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

### <span data-ttu-id="d75b7-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="d75b7-114">-VMName</span></span>
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

### <span data-ttu-id="d75b7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75b7-115">CommonParameters</span></span>
<span data-ttu-id="d75b7-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75b7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75b7-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d75b7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75b7-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d75b7-118">INPUTS</span></span>

### <span data-ttu-id="d75b7-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="d75b7-119">None</span></span>
<span data-ttu-id="d75b7-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d75b7-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d75b7-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d75b7-121">OUTPUTS</span></span>

### <span data-ttu-id="d75b7-122">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d75b7-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d75b7-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d75b7-123">NOTES</span></span>

## <span data-ttu-id="d75b7-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d75b7-124">RELATED LINKS</span></span>

