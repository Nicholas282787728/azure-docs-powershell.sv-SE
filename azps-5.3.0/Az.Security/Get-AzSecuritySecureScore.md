---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525645"
---
# <span data-ttu-id="609a3-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="609a3-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="609a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="609a3-102">SYNOPSIS</span></span>
<span data-ttu-id="609a3-103">Får säkra poäng och deras resultat för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="609a3-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="609a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="609a3-104">SYNTAX</span></span>

### <span data-ttu-id="609a3-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="609a3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="609a3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="609a3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="609a3-107">EXAMPLES</span></span>

### <span data-ttu-id="609a3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="609a3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="609a3-109">Får alla säkra säkerhets Poäng i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="609a3-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="609a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="609a3-110">PARAMETERS</span></span>

### <span data-ttu-id="609a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609a3-111">-DefaultProfile</span></span>
<span data-ttu-id="609a3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="609a3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="609a3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="609a3-113">-Name</span></span>
<span data-ttu-id="609a3-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="609a3-114">Resource name.</span></span>

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

### <span data-ttu-id="609a3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609a3-115">CommonParameters</span></span>
<span data-ttu-id="609a3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609a3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609a3-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="609a3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609a3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="609a3-118">INPUTS</span></span>

### <span data-ttu-id="609a3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="609a3-119">System.String</span></span>

## <span data-ttu-id="609a3-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="609a3-120">OUTPUTS</span></span>

### <span data-ttu-id="609a3-121">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="609a3-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="609a3-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="609a3-122">NOTES</span></span>

## <span data-ttu-id="609a3-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="609a3-123">RELATED LINKS</span></span>
