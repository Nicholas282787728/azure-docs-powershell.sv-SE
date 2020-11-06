---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575652"
---
# <span data-ttu-id="28019-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="28019-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="28019-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28019-102">SYNOPSIS</span></span>
<span data-ttu-id="28019-103">Tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="28019-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28019-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28019-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28019-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28019-105">DESCRIPTION</span></span>
<span data-ttu-id="28019-106">Cmdleten **Remove-AzureRmLogProfile** tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="28019-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="28019-107">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="28019-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="28019-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28019-108">EXAMPLES</span></span>

## <span data-ttu-id="28019-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28019-109">PARAMETERS</span></span>

### <span data-ttu-id="28019-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28019-110">-DefaultProfile</span></span>
<span data-ttu-id="28019-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="28019-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28019-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="28019-112">-Name</span></span>
<span data-ttu-id="28019-113">Anger namnet på den logg profil som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="28019-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28019-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28019-114">-PassThru</span></span>
<span data-ttu-id="28019-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="28019-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28019-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28019-116">CommonParameters</span></span>
<span data-ttu-id="28019-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28019-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28019-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28019-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28019-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28019-119">INPUTS</span></span>

### <span data-ttu-id="28019-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="28019-120">None</span></span>
<span data-ttu-id="28019-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="28019-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28019-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28019-122">OUTPUTS</span></span>

### <span data-ttu-id="28019-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="28019-123">AzureOperationResponse</span></span>

## <span data-ttu-id="28019-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28019-124">NOTES</span></span>

## <span data-ttu-id="28019-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28019-125">RELATED LINKS</span></span>

[<span data-ttu-id="28019-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="28019-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="28019-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="28019-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


