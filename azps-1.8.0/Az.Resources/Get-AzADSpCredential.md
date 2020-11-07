---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 5307e070f8c568473e1ce35f1183517cd3def05c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747175"
---
# <span data-ttu-id="06642-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="06642-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="06642-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06642-102">SYNOPSIS</span></span>
<span data-ttu-id="06642-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="06642-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="06642-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06642-104">SYNTAX</span></span>

### <span data-ttu-id="06642-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="06642-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06642-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="06642-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06642-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06642-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06642-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06642-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06642-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06642-109">DESCRIPTION</span></span>
<span data-ttu-id="06642-110">Get-AzADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="06642-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="06642-111">Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="06642-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="06642-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06642-112">EXAMPLES</span></span>

### <span data-ttu-id="06642-113">Exempel 1 – Visa autentiseringsuppgifter via SPN</span><span class="sxs-lookup"><span data-stu-id="06642-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="06642-114">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="06642-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="06642-115">Exempel 2 – Visa autentiseringsuppgifter utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="06642-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="06642-116">Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="06642-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="06642-117">Exempel 3 – Visa autentiseringsuppgifter efter ledning</span><span class="sxs-lookup"><span data-stu-id="06642-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="06642-118">Hämtar tjänstens huvud namn med objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" och kopplas till Get-AzADSpCredential cmdlet för att lista alla autentiseringsuppgifter för det tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="06642-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="06642-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06642-119">PARAMETERS</span></span>

### <span data-ttu-id="06642-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06642-120">-DefaultProfile</span></span>
<span data-ttu-id="06642-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="06642-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06642-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06642-122">-DisplayName</span></span>
<span data-ttu-id="06642-123">Visnings namnet på tjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="06642-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="06642-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="06642-124">-ObjectId</span></span>
<span data-ttu-id="06642-125">Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="06642-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06642-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="06642-126">-ServicePrincipalName</span></span>
<span data-ttu-id="06642-127">Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="06642-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="06642-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="06642-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="06642-129">Tjänst huvud objekt som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="06642-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06642-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06642-130">CommonParameters</span></span>
<span data-ttu-id="06642-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06642-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06642-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06642-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06642-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06642-133">INPUTS</span></span>

### <span data-ttu-id="06642-134">System. String</span><span class="sxs-lookup"><span data-stu-id="06642-134">System.String</span></span>

### <span data-ttu-id="06642-135">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="06642-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="06642-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06642-136">OUTPUTS</span></span>

### <span data-ttu-id="06642-137">Microsoft. Azure. commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="06642-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="06642-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06642-138">NOTES</span></span>

## <span data-ttu-id="06642-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06642-139">RELATED LINKS</span></span>

[<span data-ttu-id="06642-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="06642-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="06642-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="06642-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="06642-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="06642-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

