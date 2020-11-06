---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576798"
---
# <span data-ttu-id="1cdfb-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1cdfb-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="1cdfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cdfb-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdfb-103">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cdfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cdfb-104">SYNTAX</span></span>

### <span data-ttu-id="1cdfb-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1cdfb-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1cdfb-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cdfb-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1cdfb-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cdfb-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1cdfb-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cdfb-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1cdfb-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cdfb-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1cdfb-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cdfb-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1cdfb-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cdfb-111">DESCRIPTION</span></span>
<span data-ttu-id="1cdfb-112">Visar befintliga Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="1cdfb-113">Program uppslag kan utföras av ObjectId, ApplicationId, IdentifierUri eller DisplayName.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="1cdfb-114">Om ingen parameter anges hämtar den alla program under innehavaren.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="1cdfb-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cdfb-115">EXAMPLES</span></span>

### <span data-ttu-id="1cdfb-116">Exempel 1 – Visa alla program</span><span class="sxs-lookup"><span data-stu-id="1cdfb-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="1cdfb-117">Visar alla program under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="1cdfb-118">Exempel 2-lista med program som använder sid indelning</span><span class="sxs-lookup"><span data-stu-id="1cdfb-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="1cdfb-119">Visar de första 100-programmen under en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="1cdfb-120">Exempel 3 – få program utifrån ID URI</span><span class="sxs-lookup"><span data-stu-id="1cdfb-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="1cdfb-121">Hämtar programmet med ID-URI som " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="1cdfb-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="1cdfb-122">Exempel 4 – Hämta program utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="1cdfb-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="1cdfb-123">Hämtar programmet med objekt-ID ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 '.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="1cdfb-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cdfb-124">PARAMETERS</span></span>

### <span data-ttu-id="1cdfb-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1cdfb-125">-ApplicationId</span></span>
<span data-ttu-id="1cdfb-126">Program-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="1cdfb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdfb-127">-DefaultProfile</span></span>
<span data-ttu-id="1cdfb-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1cdfb-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cdfb-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1cdfb-129">-DisplayName</span></span>
<span data-ttu-id="1cdfb-130">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-130">The display name of the application.</span></span>

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

### <span data-ttu-id="1cdfb-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="1cdfb-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="1cdfb-132">Hämta alla program som börjar med visnings namnet.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="1cdfb-133">-Först</span><span class="sxs-lookup"><span data-stu-id="1cdfb-133">-First</span></span>
<span data-ttu-id="1cdfb-134">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1cdfb-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1cdfb-135">-IdentifierUri</span></span>
<span data-ttu-id="1cdfb-136">Unik ID URI för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="1cdfb-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1cdfb-137">-IncludeTotalCount</span></span>
<span data-ttu-id="1cdfb-138">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1cdfb-139">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1cdfb-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1cdfb-140">-ObjectId</span></span>
<span data-ttu-id="1cdfb-141">Objekt-ID för programmet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="1cdfb-142">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1cdfb-142">-Skip</span></span>
<span data-ttu-id="1cdfb-143">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1cdfb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdfb-144">CommonParameters</span></span>
<span data-ttu-id="1cdfb-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cdfb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdfb-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cdfb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdfb-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cdfb-147">INPUTS</span></span>

### <span data-ttu-id="1cdfb-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1cdfb-148">System.Guid</span></span>

### <span data-ttu-id="1cdfb-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1cdfb-149">System.String</span></span>

## <span data-ttu-id="1cdfb-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cdfb-150">OUTPUTS</span></span>

### <span data-ttu-id="1cdfb-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1cdfb-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="1cdfb-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cdfb-152">NOTES</span></span>

## <span data-ttu-id="1cdfb-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cdfb-153">RELATED LINKS</span></span>

[<span data-ttu-id="1cdfb-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1cdfb-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="1cdfb-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1cdfb-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="1cdfb-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1cdfb-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="1cdfb-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1cdfb-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="1cdfb-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1cdfb-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="1cdfb-159">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1cdfb-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

