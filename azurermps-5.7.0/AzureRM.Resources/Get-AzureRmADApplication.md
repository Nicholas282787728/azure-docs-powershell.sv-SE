---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582011"
---
# <span data-ttu-id="72765-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="72765-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="72765-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72765-102">SYNOPSIS</span></span>
<span data-ttu-id="72765-103">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="72765-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72765-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72765-104">SYNTAX</span></span>

### <span data-ttu-id="72765-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72765-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72765-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72765-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72765-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72765-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72765-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="72765-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72765-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="72765-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72765-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72765-110">DESCRIPTION</span></span>
<span data-ttu-id="72765-111">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="72765-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="72765-112">Program uppslag kan utföras av ObjectId, ApplicationId, IdentifierUri eller DisplayName.</span><span class="sxs-lookup"><span data-stu-id="72765-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="72765-113">Om ingen parameter anges hämtar den alla program under innehavaren.</span><span class="sxs-lookup"><span data-stu-id="72765-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="72765-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72765-114">EXAMPLES</span></span>

### <span data-ttu-id="72765-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72765-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="72765-116">Visar alla program under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="72765-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="72765-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="72765-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="72765-118">Hämtar programmet med ID-URI som " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="72765-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="72765-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72765-119">PARAMETERS</span></span>

### <span data-ttu-id="72765-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="72765-120">-ApplicationId</span></span>
<span data-ttu-id="72765-121">Program-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="72765-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72765-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72765-122">-DefaultProfile</span></span>
<span data-ttu-id="72765-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72765-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72765-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="72765-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="72765-125">Hämta alla program som börjar med visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="72765-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72765-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="72765-126">-IdentifierUri</span></span>
<span data-ttu-id="72765-127">Unik ID URI för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="72765-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72765-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="72765-128">-ObjectId</span></span>
<span data-ttu-id="72765-129">Objekt-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="72765-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72765-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72765-130">CommonParameters</span></span>
<span data-ttu-id="72765-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72765-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72765-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72765-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72765-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72765-133">INPUTS</span></span>

### <span data-ttu-id="72765-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="72765-134">None</span></span>
<span data-ttu-id="72765-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="72765-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72765-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72765-136">OUTPUTS</span></span>

### <span data-ttu-id="72765-137">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="72765-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="72765-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72765-138">NOTES</span></span>

## <span data-ttu-id="72765-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72765-139">RELATED LINKS</span></span>

[<span data-ttu-id="72765-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="72765-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="72765-141">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="72765-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="72765-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="72765-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="72765-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="72765-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="72765-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="72765-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="72765-145">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="72765-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

