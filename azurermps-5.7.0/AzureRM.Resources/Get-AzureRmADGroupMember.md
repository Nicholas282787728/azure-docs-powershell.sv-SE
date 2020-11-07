---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756784"
---
# <span data-ttu-id="3721c-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="3721c-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="3721c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3721c-102">SYNOPSIS</span></span>
<span data-ttu-id="3721c-103">Skaffa grupp medlemmar.</span><span class="sxs-lookup"><span data-stu-id="3721c-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3721c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3721c-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3721c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3721c-105">DESCRIPTION</span></span>
<span data-ttu-id="3721c-106">Skaffa grupp medlemmar.</span><span class="sxs-lookup"><span data-stu-id="3721c-106">Get a group members.</span></span>

## <span data-ttu-id="3721c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3721c-107">EXAMPLES</span></span>

### <span data-ttu-id="3721c-108">Filtrerar grupp medlemmar med hjälp av grupp objekt-ID</span><span class="sxs-lookup"><span data-stu-id="3721c-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3721c-109">Hämtar grupp medlemmar med 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID</span><span class="sxs-lookup"><span data-stu-id="3721c-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="3721c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3721c-110">PARAMETERS</span></span>

### <span data-ttu-id="3721c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3721c-111">-DefaultProfile</span></span>
<span data-ttu-id="3721c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3721c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3721c-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="3721c-113">-GroupObjectId</span></span>
<span data-ttu-id="3721c-114">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="3721c-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3721c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3721c-115">CommonParameters</span></span>
<span data-ttu-id="3721c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3721c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3721c-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3721c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3721c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3721c-118">INPUTS</span></span>

### <span data-ttu-id="3721c-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="3721c-119">None</span></span>
<span data-ttu-id="3721c-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3721c-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3721c-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3721c-121">OUTPUTS</span></span>

### <span data-ttu-id="3721c-122">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="3721c-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="3721c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3721c-123">NOTES</span></span>

## <span data-ttu-id="3721c-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3721c-124">RELATED LINKS</span></span>

[<span data-ttu-id="3721c-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="3721c-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="3721c-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3721c-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

