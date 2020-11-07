---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: a0f4c41b310e820b939500b8496b411d7b0266d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930113"
---
# <span data-ttu-id="42f98-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="42f98-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="42f98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42f98-102">SYNOPSIS</span></span>
<span data-ttu-id="42f98-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="42f98-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42f98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42f98-104">SYNTAX</span></span>

### <span data-ttu-id="42f98-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42f98-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42f98-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="42f98-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42f98-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42f98-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42f98-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42f98-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f98-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42f98-109">DESCRIPTION</span></span>
<span data-ttu-id="42f98-110">Get-AzureRmADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="42f98-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="42f98-111">Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="42f98-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="42f98-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42f98-112">EXAMPLES</span></span>

### <span data-ttu-id="42f98-113">Exempel 1 – Visa autentiseringsuppgifter via SPN</span><span class="sxs-lookup"><span data-stu-id="42f98-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="42f98-114">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="42f98-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="42f98-115">Exempel 2 – Visa autentiseringsuppgifter utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="42f98-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="42f98-116">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="42f98-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="42f98-117">Exempel 3 – Visa autentiseringsuppgifter efter ledning</span><span class="sxs-lookup"><span data-stu-id="42f98-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="42f98-118">Hämtar tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" och kopplas till Get-AzureRmADSpCredential cmdlet för att lista alla autentiseringsuppgifter för det tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="42f98-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="42f98-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42f98-119">PARAMETERS</span></span>

### <span data-ttu-id="42f98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f98-120">-DefaultProfile</span></span>
<span data-ttu-id="42f98-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="42f98-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f98-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="42f98-122">-DisplayName</span></span>
<span data-ttu-id="42f98-123">Visnings namnet på tjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="42f98-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="42f98-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="42f98-124">-ObjectId</span></span>
<span data-ttu-id="42f98-125">Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="42f98-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="42f98-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="42f98-126">-ServicePrincipalName</span></span>
<span data-ttu-id="42f98-127">Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="42f98-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="42f98-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="42f98-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="42f98-129">Tjänst huvud objekt som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="42f98-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="42f98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f98-130">CommonParameters</span></span>
<span data-ttu-id="42f98-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f98-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f98-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f98-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42f98-133">INPUTS</span></span>

### <span data-ttu-id="42f98-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="42f98-134">System.Guid</span></span>

### <span data-ttu-id="42f98-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42f98-135">System.String</span></span>

### <span data-ttu-id="42f98-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="42f98-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="42f98-137">Parametrar: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42f98-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="42f98-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42f98-138">OUTPUTS</span></span>

### <span data-ttu-id="42f98-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="42f98-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="42f98-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42f98-140">NOTES</span></span>

## <span data-ttu-id="42f98-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42f98-141">RELATED LINKS</span></span>

[<span data-ttu-id="42f98-142">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="42f98-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="42f98-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="42f98-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="42f98-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="42f98-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

