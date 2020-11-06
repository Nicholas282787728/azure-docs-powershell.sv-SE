---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582007"
---
# <span data-ttu-id="504c2-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="504c2-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="504c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="504c2-102">SYNOPSIS</span></span>
<span data-ttu-id="504c2-103">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="504c2-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="504c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="504c2-104">SYNTAX</span></span>

### <span data-ttu-id="504c2-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="504c2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="504c2-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="504c2-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="504c2-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="504c2-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="504c2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="504c2-108">DESCRIPTION</span></span>
<span data-ttu-id="504c2-109">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="504c2-109">Filters active directory groups.</span></span>

## <span data-ttu-id="504c2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="504c2-110">EXAMPLES</span></span>

### <span data-ttu-id="504c2-111">Filtrerar grupper med objekt-ID</span><span class="sxs-lookup"><span data-stu-id="504c2-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="504c2-112">Hämtar grupp med 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID</span><span class="sxs-lookup"><span data-stu-id="504c2-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="504c2-113">Filtrerar grupper med Sök sträng</span><span class="sxs-lookup"><span data-stu-id="504c2-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="504c2-114">Filtrerar alla AD-grupper som har Joe i visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="504c2-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="504c2-115">Visa en lista över AD-grupper</span><span class="sxs-lookup"><span data-stu-id="504c2-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="504c2-116">Får alla AD-grupper</span><span class="sxs-lookup"><span data-stu-id="504c2-116">Gets all AD groups</span></span>

## <span data-ttu-id="504c2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="504c2-117">PARAMETERS</span></span>

### <span data-ttu-id="504c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504c2-118">-DefaultProfile</span></span>
<span data-ttu-id="504c2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="504c2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="504c2-120">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="504c2-120">-ObjectId</span></span>
<span data-ttu-id="504c2-121">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="504c2-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504c2-122">-SearchString</span><span class="sxs-lookup"><span data-stu-id="504c2-122">-SearchString</span></span>
<span data-ttu-id="504c2-123">Gruppens visnings namn</span><span class="sxs-lookup"><span data-stu-id="504c2-123">The group display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504c2-124">CommonParameters</span></span>
<span data-ttu-id="504c2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="504c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504c2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="504c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504c2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="504c2-127">INPUTS</span></span>

### <span data-ttu-id="504c2-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="504c2-128">None</span></span>
<span data-ttu-id="504c2-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="504c2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="504c2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="504c2-130">OUTPUTS</span></span>

### <span data-ttu-id="504c2-131">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="504c2-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="504c2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="504c2-132">NOTES</span></span>

## <span data-ttu-id="504c2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="504c2-133">RELATED LINKS</span></span>

[<span data-ttu-id="504c2-134">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="504c2-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="504c2-135">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="504c2-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="504c2-136">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="504c2-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

