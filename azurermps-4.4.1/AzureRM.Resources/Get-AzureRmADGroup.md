---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575862"
---
# <span data-ttu-id="0510f-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="0510f-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="0510f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0510f-102">SYNOPSIS</span></span>
<span data-ttu-id="0510f-103">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="0510f-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0510f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0510f-104">SYNTAX</span></span>

### <span data-ttu-id="0510f-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0510f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0510f-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0510f-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0510f-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0510f-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0510f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0510f-108">DESCRIPTION</span></span>
<span data-ttu-id="0510f-109">Filtrerar Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="0510f-109">Filters active directory groups.</span></span>

## <span data-ttu-id="0510f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0510f-110">EXAMPLES</span></span>

### <span data-ttu-id="0510f-111">--------------------------Filtrerar grupper med objekt-ID--------------------------</span><span class="sxs-lookup"><span data-stu-id="0510f-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="0510f-112">Hämtar grupp med 85F89C90-780E-4AA6-9F4F-6F268D322EEE-ID</span><span class="sxs-lookup"><span data-stu-id="0510f-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="0510f-113">--------------------------Filtrerar grupper med Sök sträng--------------------------</span><span class="sxs-lookup"><span data-stu-id="0510f-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="0510f-114">Filtrerar alla AD-grupper som har Joe i visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="0510f-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="0510f-115">--------------------------Lista AD-grupper--------------------------</span><span class="sxs-lookup"><span data-stu-id="0510f-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="0510f-116">Får alla AD-grupper</span><span class="sxs-lookup"><span data-stu-id="0510f-116">Gets all AD groups</span></span>

## <span data-ttu-id="0510f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0510f-117">PARAMETERS</span></span>

### <span data-ttu-id="0510f-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0510f-118">-ObjectId</span></span>
<span data-ttu-id="0510f-119">Objekt-ID för gruppen.</span><span class="sxs-lookup"><span data-stu-id="0510f-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510f-120">-SearchString</span><span class="sxs-lookup"><span data-stu-id="0510f-120">-SearchString</span></span>
<span data-ttu-id="0510f-121">Gruppens visnings namn</span><span class="sxs-lookup"><span data-stu-id="0510f-121">The group display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0510f-122">-DefaultProfile</span></span>
<span data-ttu-id="0510f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0510f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0510f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0510f-124">CommonParameters</span></span>
<span data-ttu-id="0510f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0510f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0510f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0510f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0510f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0510f-127">INPUTS</span></span>

## <span data-ttu-id="0510f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0510f-128">OUTPUTS</span></span>

### <span data-ttu-id="0510f-129">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="0510f-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="0510f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0510f-130">NOTES</span></span>

## <span data-ttu-id="0510f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0510f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0510f-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0510f-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="0510f-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0510f-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0510f-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="0510f-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

