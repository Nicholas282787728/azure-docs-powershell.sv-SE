---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756599"
---
# <span data-ttu-id="335be-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="335be-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="335be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="335be-102">SYNOPSIS</span></span>
<span data-ttu-id="335be-103">Tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="335be-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="335be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="335be-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="335be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="335be-105">DESCRIPTION</span></span>
<span data-ttu-id="335be-106">Cmdleten **Remove-AzureRmLogProfile** tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="335be-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="335be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="335be-107">EXAMPLES</span></span>

## <span data-ttu-id="335be-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="335be-108">PARAMETERS</span></span>

### <span data-ttu-id="335be-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="335be-109">-Name</span></span>
<span data-ttu-id="335be-110">Anger namnet på den logg profil som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="335be-110">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335be-111">-DefaultProfile</span></span>
<span data-ttu-id="335be-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="335be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="335be-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="335be-113">-PassThru</span></span>
<span data-ttu-id="335be-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="335be-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="335be-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335be-115">CommonParameters</span></span>
<span data-ttu-id="335be-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335be-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335be-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335be-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335be-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="335be-118">INPUTS</span></span>

## <span data-ttu-id="335be-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="335be-119">OUTPUTS</span></span>

### <span data-ttu-id="335be-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="335be-120">System.Boolean</span></span>

## <span data-ttu-id="335be-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="335be-121">NOTES</span></span>

## <span data-ttu-id="335be-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="335be-122">RELATED LINKS</span></span>

[<span data-ttu-id="335be-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="335be-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="335be-124">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="335be-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


