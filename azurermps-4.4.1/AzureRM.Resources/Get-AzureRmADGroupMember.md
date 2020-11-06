---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: 17d7f922f5af46aa99e3b01aa0c0f63df05effe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575859"
---
# <span data-ttu-id="6c12c-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="6c12c-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="6c12c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c12c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c12c-103">Skaffa grupp medlemmar.</span><span class="sxs-lookup"><span data-stu-id="6c12c-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c12c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c12c-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c12c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c12c-105">DESCRIPTION</span></span>
<span data-ttu-id="6c12c-106">Skaffa grupp medlemmar.</span><span class="sxs-lookup"><span data-stu-id="6c12c-106">Get a group members.</span></span>

## <span data-ttu-id="6c12c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c12c-107">EXAMPLES</span></span>

### <span data-ttu-id="6c12c-108">--------------------------Filtrerar grupp medlemmar med grupp objekt-ID--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c12c-108">--------------------------  Filters group members using group object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6c12c-109">Hämtar grupp medlemmar med 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID</span><span class="sxs-lookup"><span data-stu-id="6c12c-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="6c12c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c12c-110">PARAMETERS</span></span>

### <span data-ttu-id="6c12c-111">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="6c12c-111">-GroupObjectId</span></span>
<span data-ttu-id="6c12c-112">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="6c12c-112">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c12c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c12c-113">-DefaultProfile</span></span>
<span data-ttu-id="6c12c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c12c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c12c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c12c-115">CommonParameters</span></span>
<span data-ttu-id="6c12c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c12c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c12c-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c12c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c12c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c12c-118">INPUTS</span></span>

## <span data-ttu-id="6c12c-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c12c-119">OUTPUTS</span></span>

### <span data-ttu-id="6c12c-120">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="6c12c-120">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="6c12c-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c12c-121">NOTES</span></span>

## <span data-ttu-id="6c12c-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c12c-122">RELATED LINKS</span></span>

[<span data-ttu-id="6c12c-123">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6c12c-123">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="6c12c-124">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6c12c-124">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

