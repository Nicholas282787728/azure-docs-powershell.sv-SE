---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755925"
---
# <span data-ttu-id="1fd73-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1fd73-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="1fd73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fd73-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd73-103">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1fd73-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fd73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fd73-104">SYNTAX</span></span>

### <span data-ttu-id="1fd73-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1fd73-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd73-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd73-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd73-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd73-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd73-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd73-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fd73-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd73-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fd73-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fd73-110">DESCRIPTION</span></span>
<span data-ttu-id="1fd73-111">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1fd73-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="1fd73-112">Program uppslag kan utföras av ObjectId, ApplicationId, IdentifierUri eller DisplayName.</span><span class="sxs-lookup"><span data-stu-id="1fd73-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="1fd73-113">Om ingen parameter anges hämtar den alla program under innehavaren.</span><span class="sxs-lookup"><span data-stu-id="1fd73-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="1fd73-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fd73-114">EXAMPLES</span></span>

### <span data-ttu-id="1fd73-115">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1fd73-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="1fd73-116">Visar alla program under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1fd73-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="1fd73-117">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1fd73-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="1fd73-118">Hämtar programmet med ID-URI som " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="1fd73-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="1fd73-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fd73-119">PARAMETERS</span></span>

### <span data-ttu-id="1fd73-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1fd73-120">-ApplicationId</span></span>
<span data-ttu-id="1fd73-121">Program-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1fd73-121">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd73-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="1fd73-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="1fd73-123">Hämta alla program som börjar med visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="1fd73-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd73-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1fd73-124">-IdentifierUri</span></span>
<span data-ttu-id="1fd73-125">Unik ID URI för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1fd73-125">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd73-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1fd73-126">-ObjectId</span></span>
<span data-ttu-id="1fd73-127">Objekt-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1fd73-127">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd73-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd73-128">-DefaultProfile</span></span>
<span data-ttu-id="1fd73-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd73-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fd73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd73-130">CommonParameters</span></span>
<span data-ttu-id="1fd73-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd73-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd73-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd73-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fd73-133">INPUTS</span></span>

## <span data-ttu-id="1fd73-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fd73-134">OUTPUTS</span></span>

### <span data-ttu-id="1fd73-135">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="1fd73-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="1fd73-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fd73-136">NOTES</span></span>

## <span data-ttu-id="1fd73-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fd73-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fd73-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1fd73-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="1fd73-139">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1fd73-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="1fd73-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1fd73-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="1fd73-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1fd73-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="1fd73-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1fd73-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="1fd73-143">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1fd73-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

