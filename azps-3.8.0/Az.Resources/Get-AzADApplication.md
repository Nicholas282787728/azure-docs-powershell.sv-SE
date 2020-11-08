---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: afcb95eca70c005023bacc2b2d71d9fda54c9259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089757"
---
# <span data-ttu-id="1da81-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1da81-101">Get-AzADApplication</span></span>

## <span data-ttu-id="1da81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1da81-102">SYNOPSIS</span></span>
<span data-ttu-id="1da81-103">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1da81-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="1da81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1da81-104">SYNTAX</span></span>

### <span data-ttu-id="1da81-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1da81-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1da81-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da81-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1da81-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da81-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1da81-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da81-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1da81-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da81-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1da81-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1da81-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1da81-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1da81-111">DESCRIPTION</span></span>
<span data-ttu-id="1da81-112">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1da81-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="1da81-113">Program uppslag kan utföras av ObjectId, ApplicationId, IdentifierUri eller DisplayName.</span><span class="sxs-lookup"><span data-stu-id="1da81-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="1da81-114">Om ingen parameter anges hämtar den alla program under innehavaren.</span><span class="sxs-lookup"><span data-stu-id="1da81-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="1da81-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1da81-115">EXAMPLES</span></span>

### <span data-ttu-id="1da81-116">Exempel 1 – Visa alla program</span><span class="sxs-lookup"><span data-stu-id="1da81-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="1da81-117">Visar alla program under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1da81-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="1da81-118">Exempel 2-lista med program som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="1da81-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="1da81-119">Visar de första 100-programmen under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1da81-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="1da81-120">Exempel 3 – få program utifrån ID URI</span><span class="sxs-lookup"><span data-stu-id="1da81-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="1da81-121">Hämtar programmet med ID-URI som " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="1da81-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="1da81-122">Exempel 4 – Hämta program utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="1da81-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="1da81-123">Hämtar programmet med objekt-ID ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 '.</span><span class="sxs-lookup"><span data-stu-id="1da81-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="1da81-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1da81-124">PARAMETERS</span></span>

### <span data-ttu-id="1da81-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1da81-125">-ApplicationId</span></span>
<span data-ttu-id="1da81-126">Program-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1da81-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="1da81-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da81-127">-DefaultProfile</span></span>
<span data-ttu-id="1da81-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1da81-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1da81-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1da81-129">-DisplayName</span></span>
<span data-ttu-id="1da81-130">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="1da81-130">The display name of the application.</span></span>

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

### <span data-ttu-id="1da81-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="1da81-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="1da81-132">Hämta alla program som börjar med visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="1da81-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="1da81-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1da81-133">-IdentifierUri</span></span>
<span data-ttu-id="1da81-134">Unik ID URI för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1da81-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="1da81-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1da81-135">-ObjectId</span></span>
<span data-ttu-id="1da81-136">Objekt-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1da81-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="1da81-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1da81-137">-IncludeTotalCount</span></span>
<span data-ttu-id="1da81-138">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1da81-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1da81-139">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="1da81-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1da81-140">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1da81-140">-Skip</span></span>
<span data-ttu-id="1da81-141">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="1da81-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1da81-142">-Först</span><span class="sxs-lookup"><span data-stu-id="1da81-142">-First</span></span>
<span data-ttu-id="1da81-143">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="1da81-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1da81-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da81-144">CommonParameters</span></span>
<span data-ttu-id="1da81-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da81-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da81-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1da81-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da81-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1da81-147">INPUTS</span></span>

### <span data-ttu-id="1da81-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1da81-148">System.String</span></span>

### <span data-ttu-id="1da81-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1da81-149">System.Guid</span></span>

## <span data-ttu-id="1da81-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1da81-150">OUTPUTS</span></span>

### <span data-ttu-id="1da81-151">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1da81-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="1da81-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1da81-152">NOTES</span></span>

## <span data-ttu-id="1da81-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1da81-153">RELATED LINKS</span></span>

[<span data-ttu-id="1da81-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1da81-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="1da81-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1da81-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="1da81-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1da81-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="1da81-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1da81-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="1da81-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1da81-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="1da81-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1da81-159">New-AzADApplication</span></span>](./New-AzADApplication.md)
