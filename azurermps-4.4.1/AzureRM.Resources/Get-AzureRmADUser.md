---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574536"
---
# <span data-ttu-id="97b51-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="97b51-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="97b51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97b51-102">SYNOPSIS</span></span>
<span data-ttu-id="97b51-103">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="97b51-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97b51-104">SYNTAX</span></span>

### <span data-ttu-id="97b51-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="97b51-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b51-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b51-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b51-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b51-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b51-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b51-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b51-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b51-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97b51-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97b51-110">DESCRIPTION</span></span>
<span data-ttu-id="97b51-111">Filtrerar Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="97b51-111">Filters active directory users.</span></span>

## <span data-ttu-id="97b51-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97b51-112">EXAMPLES</span></span>

### <span data-ttu-id="97b51-113">--------------------------Filtrerar användare med UPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="97b51-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="97b51-114">Får användare med foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="97b51-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="97b51-115">--------------------------Filtrerar användare med Sök strängar--------------------------</span><span class="sxs-lookup"><span data-stu-id="97b51-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="97b51-116">Filtrerar alla AD-användare som har Joe i visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="97b51-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="97b51-117">--------------------------Lista AD-användare--------------------------</span><span class="sxs-lookup"><span data-stu-id="97b51-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="97b51-118">Får alla AD-användare</span><span class="sxs-lookup"><span data-stu-id="97b51-118">Gets all AD users</span></span>

## <span data-ttu-id="97b51-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97b51-119">PARAMETERS</span></span>

### <span data-ttu-id="97b51-120">-E-post</span><span class="sxs-lookup"><span data-stu-id="97b51-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b51-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="97b51-121">-ObjectId</span></span>
<span data-ttu-id="97b51-122">Användarens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="97b51-122">Object id of the user.</span></span>

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

### <span data-ttu-id="97b51-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="97b51-123">-SearchString</span></span>
<span data-ttu-id="97b51-124">Användarens visnings namn</span><span class="sxs-lookup"><span data-stu-id="97b51-124">The user display name</span></span>

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

### <span data-ttu-id="97b51-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="97b51-125">-UserPrincipalName</span></span>
<span data-ttu-id="97b51-126">Användarens UPN.</span><span class="sxs-lookup"><span data-stu-id="97b51-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b51-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b51-127">-DefaultProfile</span></span>
<span data-ttu-id="97b51-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97b51-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b51-129">CommonParameters</span></span>
<span data-ttu-id="97b51-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b51-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b51-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b51-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97b51-132">INPUTS</span></span>

## <span data-ttu-id="97b51-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97b51-133">OUTPUTS</span></span>

### <span data-ttu-id="97b51-134">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="97b51-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="97b51-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97b51-135">NOTES</span></span>

## <span data-ttu-id="97b51-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97b51-136">RELATED LINKS</span></span>

[<span data-ttu-id="97b51-137">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="97b51-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="97b51-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="97b51-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="97b51-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="97b51-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

