---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 18b5f64426b0a3c458ea489d27781f1a01336b52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747187"
---
# <span data-ttu-id="c7ae1-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c7ae1-101">Get-AzADApplication</span></span>

## <span data-ttu-id="c7ae1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ae1-103">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="c7ae1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7ae1-104">SYNTAX</span></span>

### <span data-ttu-id="c7ae1-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7ae1-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c7ae1-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ae1-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c7ae1-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ae1-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c7ae1-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ae1-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c7ae1-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ae1-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c7ae1-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ae1-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c7ae1-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7ae1-111">DESCRIPTION</span></span>
<span data-ttu-id="c7ae1-112">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="c7ae1-113">Program uppslag kan utföras av ObjectId, ApplicationId, IdentifierUri eller DisplayName.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="c7ae1-114">Om ingen parameter anges hämtar den alla program under innehavaren.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="c7ae1-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7ae1-115">EXAMPLES</span></span>

### <span data-ttu-id="c7ae1-116">Exempel 1 – Visa alla program</span><span class="sxs-lookup"><span data-stu-id="c7ae1-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="c7ae1-117">Visar alla program under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="c7ae1-118">Exempel 2-lista med program som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="c7ae1-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="c7ae1-119">Visar de första 100-programmen under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="c7ae1-120">Exempel 3 – få program utifrån ID URI</span><span class="sxs-lookup"><span data-stu-id="c7ae1-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="c7ae1-121">Hämtar programmet med ID-URI som " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="c7ae1-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="c7ae1-122">Exempel 4 – Hämta program utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="c7ae1-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="c7ae1-123">Hämtar programmet med objekt-ID ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 '.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="c7ae1-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7ae1-124">PARAMETERS</span></span>

### <span data-ttu-id="c7ae1-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7ae1-125">-ApplicationId</span></span>
<span data-ttu-id="c7ae1-126">Program-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="c7ae1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ae1-127">-DefaultProfile</span></span>
<span data-ttu-id="c7ae1-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c7ae1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7ae1-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7ae1-129">-DisplayName</span></span>
<span data-ttu-id="c7ae1-130">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-130">The display name of the application.</span></span>

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

### <span data-ttu-id="c7ae1-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="c7ae1-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="c7ae1-132">Hämta alla program som börjar med visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="c7ae1-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c7ae1-133">-IdentifierUri</span></span>
<span data-ttu-id="c7ae1-134">Unik ID URI för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="c7ae1-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7ae1-135">-ObjectId</span></span>
<span data-ttu-id="c7ae1-136">Objekt-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ae1-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c7ae1-137">-IncludeTotalCount</span></span>
<span data-ttu-id="c7ae1-138">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c7ae1-139">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-139">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ae1-140">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="c7ae1-140">-Skip</span></span>
<span data-ttu-id="c7ae1-141">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ae1-142">-Först</span><span class="sxs-lookup"><span data-stu-id="c7ae1-142">-First</span></span>
<span data-ttu-id="c7ae1-143">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ae1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ae1-144">CommonParameters</span></span>
<span data-ttu-id="c7ae1-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ae1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ae1-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ae1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ae1-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7ae1-147">INPUTS</span></span>

### <span data-ttu-id="c7ae1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c7ae1-148">System.String</span></span>

### <span data-ttu-id="c7ae1-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c7ae1-149">System.Guid</span></span>

## <span data-ttu-id="c7ae1-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7ae1-150">OUTPUTS</span></span>

### <span data-ttu-id="c7ae1-151">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c7ae1-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c7ae1-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7ae1-152">NOTES</span></span>

## <span data-ttu-id="c7ae1-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7ae1-153">RELATED LINKS</span></span>

[<span data-ttu-id="c7ae1-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7ae1-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="c7ae1-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7ae1-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c7ae1-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7ae1-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c7ae1-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c7ae1-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c7ae1-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c7ae1-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="c7ae1-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c7ae1-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

