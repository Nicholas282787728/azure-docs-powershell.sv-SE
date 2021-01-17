---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420971"
---
# <span data-ttu-id="4ed70-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="4ed70-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="4ed70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ed70-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed70-103">Hämtar kontroller för säker Poäng och deras resultat för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4ed70-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="4ed70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ed70-104">SYNTAX</span></span>

### <span data-ttu-id="4ed70-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="4ed70-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed70-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4ed70-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed70-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ed70-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed70-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ed70-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="4ed70-109">Får alla säkra säkerhets Poäng i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4ed70-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="4ed70-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ed70-110">PARAMETERS</span></span>

### <span data-ttu-id="4ed70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed70-111">-DefaultProfile</span></span>
<span data-ttu-id="4ed70-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed70-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ed70-113">-Name</span></span>
<span data-ttu-id="4ed70-114">Säkert Poäng namn.</span><span class="sxs-lookup"><span data-stu-id="4ed70-114">Secure score name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed70-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed70-115">CommonParameters</span></span>
<span data-ttu-id="4ed70-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed70-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed70-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ed70-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed70-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ed70-118">INPUTS</span></span>

### <span data-ttu-id="4ed70-119">System. String</span><span class="sxs-lookup"><span data-stu-id="4ed70-119">System.String</span></span>

## <span data-ttu-id="4ed70-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ed70-120">OUTPUTS</span></span>

### <span data-ttu-id="4ed70-121">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="4ed70-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="4ed70-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ed70-122">NOTES</span></span>

## <span data-ttu-id="4ed70-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ed70-123">RELATED LINKS</span></span>
