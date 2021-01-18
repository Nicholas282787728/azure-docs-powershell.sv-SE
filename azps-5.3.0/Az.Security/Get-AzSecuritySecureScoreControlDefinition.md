---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525644"
---
# <span data-ttu-id="645c9-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="645c9-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="645c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="645c9-102">SYNOPSIS</span></span>
<span data-ttu-id="645c9-103">Hämtar säkerhets definitioner för säker Poäng kontroll för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="645c9-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="645c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="645c9-104">SYNTAX</span></span>

### <span data-ttu-id="645c9-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="645c9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="645c9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="645c9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="645c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="645c9-107">EXAMPLES</span></span>

### <span data-ttu-id="645c9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="645c9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="645c9-109">Får alla definitioner för säker Poäng kontroll i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="645c9-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="645c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="645c9-110">PARAMETERS</span></span>

### <span data-ttu-id="645c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645c9-111">-DefaultProfile</span></span>
<span data-ttu-id="645c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="645c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="645c9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645c9-113">CommonParameters</span></span>
<span data-ttu-id="645c9-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645c9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645c9-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="645c9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645c9-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="645c9-116">INPUTS</span></span>

### <span data-ttu-id="645c9-117">System. String</span><span class="sxs-lookup"><span data-stu-id="645c9-117">System.String</span></span>

## <span data-ttu-id="645c9-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="645c9-118">OUTPUTS</span></span>

### <span data-ttu-id="645c9-119">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="645c9-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="645c9-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="645c9-120">NOTES</span></span>

## <span data-ttu-id="645c9-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="645c9-121">RELATED LINKS</span></span>
