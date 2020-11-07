---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756466"
---
# <span data-ttu-id="c7136-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c7136-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="c7136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7136-102">SYNOPSIS</span></span>
<span data-ttu-id="c7136-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="c7136-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7136-104">SYNTAX</span></span>

### <span data-ttu-id="c7136-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7136-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7136-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7136-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7136-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7136-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7136-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7136-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7136-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7136-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7136-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7136-110">DESCRIPTION</span></span>
<span data-ttu-id="c7136-111">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="c7136-111">Filters active directory users.</span></span>

## <span data-ttu-id="c7136-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7136-112">EXAMPLES</span></span>

### <span data-ttu-id="c7136-113">Filtrerar användare med UPN</span><span class="sxs-lookup"><span data-stu-id="c7136-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="c7136-114">Får användare med foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="c7136-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="c7136-115">Filtrerar användare med Sök sträng</span><span class="sxs-lookup"><span data-stu-id="c7136-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="c7136-116">Filtrerar alla AD-användare som har Joe i visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="c7136-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="c7136-117">Visa en lista över AD-användare</span><span class="sxs-lookup"><span data-stu-id="c7136-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="c7136-118">Får alla AD-användare</span><span class="sxs-lookup"><span data-stu-id="c7136-118">Gets all AD users</span></span>

## <span data-ttu-id="c7136-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7136-119">PARAMETERS</span></span>

### <span data-ttu-id="c7136-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7136-120">-DefaultProfile</span></span>
<span data-ttu-id="c7136-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c7136-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7136-122">-E-post</span><span class="sxs-lookup"><span data-stu-id="c7136-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7136-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7136-123">-ObjectId</span></span>
<span data-ttu-id="c7136-124">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="c7136-124">Object id of the user.</span></span>

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

### <span data-ttu-id="c7136-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="c7136-125">-SearchString</span></span>
<span data-ttu-id="c7136-126">Användarens visnings namn</span><span class="sxs-lookup"><span data-stu-id="c7136-126">The user display name</span></span>

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

### <span data-ttu-id="c7136-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c7136-127">-UserPrincipalName</span></span>
<span data-ttu-id="c7136-128">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="c7136-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7136-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7136-129">CommonParameters</span></span>
<span data-ttu-id="c7136-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7136-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7136-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7136-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7136-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7136-132">INPUTS</span></span>

### <span data-ttu-id="c7136-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="c7136-133">None</span></span>
<span data-ttu-id="c7136-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c7136-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7136-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7136-135">OUTPUTS</span></span>

### <span data-ttu-id="c7136-136">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="c7136-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="c7136-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7136-137">NOTES</span></span>

## <span data-ttu-id="c7136-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7136-138">RELATED LINKS</span></span>

[<span data-ttu-id="c7136-139">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c7136-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="c7136-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c7136-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="c7136-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c7136-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

