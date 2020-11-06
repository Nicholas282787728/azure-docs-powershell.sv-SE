---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 72a2510c673d0e68fc3820fda7b1d99e15a6aa76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576793"
---
# <span data-ttu-id="e3096-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e3096-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="e3096-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3096-102">SYNOPSIS</span></span>
<span data-ttu-id="e3096-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="e3096-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3096-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3096-104">SYNTAX</span></span>

### <span data-ttu-id="e3096-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e3096-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3096-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3096-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3096-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3096-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3096-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3096-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3096-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3096-109">DESCRIPTION</span></span>
<span data-ttu-id="e3096-110">Get-AzureRmADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="e3096-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="e3096-111">Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e3096-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="e3096-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3096-112">EXAMPLES</span></span>

### <span data-ttu-id="e3096-113">Exempel 1 – Visa autentiseringsuppgifter via SPN</span><span class="sxs-lookup"><span data-stu-id="e3096-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="e3096-114">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="e3096-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="e3096-115">Exempel 2 – Visa autentiseringsuppgifter utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="e3096-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="e3096-116">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="e3096-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="e3096-117">Exempel 3 – Visa autentiseringsuppgifter efter ledning</span><span class="sxs-lookup"><span data-stu-id="e3096-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="e3096-118">Hämtar tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" och kopplas till Get-AzureRmADSpCredential cmdlet för att lista alla autentiseringsuppgifter för det tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="e3096-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="e3096-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3096-119">PARAMETERS</span></span>

### <span data-ttu-id="e3096-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3096-120">-DefaultProfile</span></span>
<span data-ttu-id="e3096-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3096-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3096-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3096-122">-DisplayName</span></span>
<span data-ttu-id="e3096-123">Visnings namnet på tjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="e3096-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3096-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e3096-124">-ObjectId</span></span>
<span data-ttu-id="e3096-125">Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="e3096-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3096-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e3096-126">-ServicePrincipalName</span></span>
<span data-ttu-id="e3096-127">Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="e3096-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3096-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="e3096-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="e3096-129">Tjänst huvud objekt som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="e3096-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3096-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3096-130">CommonParameters</span></span>
<span data-ttu-id="e3096-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3096-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3096-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3096-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3096-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3096-133">INPUTS</span></span>

### <span data-ttu-id="e3096-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e3096-134">System.Guid</span></span>

### <span data-ttu-id="e3096-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e3096-135">System.String</span></span>

### <span data-ttu-id="e3096-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3096-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="e3096-137">Parametrar: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3096-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="e3096-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3096-138">OUTPUTS</span></span>

### <span data-ttu-id="e3096-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e3096-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e3096-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3096-140">NOTES</span></span>

## <span data-ttu-id="e3096-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3096-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3096-142">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e3096-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="e3096-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e3096-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="e3096-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3096-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

