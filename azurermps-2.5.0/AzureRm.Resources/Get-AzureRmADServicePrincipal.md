---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929626"
---
# <span data-ttu-id="7425f-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7425f-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="7425f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7425f-102">SYNOPSIS</span></span>
<span data-ttu-id="7425f-103">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="7425f-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7425f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7425f-104">SYNTAX</span></span>

### <span data-ttu-id="7425f-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7425f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7425f-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7425f-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7425f-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7425f-112">DESCRIPTION</span></span>
<span data-ttu-id="7425f-113">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="7425f-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="7425f-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7425f-114">EXAMPLES</span></span>

### <span data-ttu-id="7425f-115">Exempel 1 – Visa AD-huvudtjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="7425f-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="7425f-116">Visar alla AD-huvudtjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="7425f-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="7425f-117">Exempel 2 – Visa AD-huvudtjänstens huvud objekt med sid indelning</span><span class="sxs-lookup"><span data-stu-id="7425f-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="7425f-118">Visar de första 100 i AD-tjänsten i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="7425f-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="7425f-119">Exempel 3-Visa tjänstens huvud namn efter SPN</span><span class="sxs-lookup"><span data-stu-id="7425f-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="7425f-120">Visar tjänstens huvud namn med SPN ' 36f81fc3-b00f-48cd-8218-3879f51ff39f '.</span><span class="sxs-lookup"><span data-stu-id="7425f-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="7425f-121">Exempel 4-lista tjänst säkerhets objekt efter Sök sträng</span><span class="sxs-lookup"><span data-stu-id="7425f-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="7425f-122">Visar alla AD-huvudobjekt vars visnings namn börjar med "webben".</span><span class="sxs-lookup"><span data-stu-id="7425f-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="7425f-123">Exempel 5 – Visa tjänst huvud objekt efter ledning</span><span class="sxs-lookup"><span data-stu-id="7425f-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="7425f-124">Hämtar AD-programmet med objekt-ID ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' och kopplas till Get-AzureRmADServicePrincipal cmdlet för att visa alla tjänstens huvud namn för det programmet.</span><span class="sxs-lookup"><span data-stu-id="7425f-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="7425f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7425f-125">PARAMETERS</span></span>

### <span data-ttu-id="7425f-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7425f-126">-ApplicationId</span></span>
<span data-ttu-id="7425f-127">Tjänstens huvud program-ID.</span><span class="sxs-lookup"><span data-stu-id="7425f-127">The service principal application id.</span></span>

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

### <span data-ttu-id="7425f-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7425f-128">-ApplicationObject</span></span>
<span data-ttu-id="7425f-129">Program objekt vars tjänste huvud hämtas.</span><span class="sxs-lookup"><span data-stu-id="7425f-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7425f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7425f-130">-DefaultProfile</span></span>
<span data-ttu-id="7425f-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7425f-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7425f-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7425f-132">-DisplayName</span></span>
<span data-ttu-id="7425f-133">Tjänstens huvud visnings namn.</span><span class="sxs-lookup"><span data-stu-id="7425f-133">The service principal display name.</span></span>

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

### <span data-ttu-id="7425f-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="7425f-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="7425f-135">Sök strängen för tjänstens huvud.</span><span class="sxs-lookup"><span data-stu-id="7425f-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7425f-136">-Först</span><span class="sxs-lookup"><span data-stu-id="7425f-136">-First</span></span>
<span data-ttu-id="7425f-137">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="7425f-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="7425f-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7425f-138">-IncludeTotalCount</span></span>
<span data-ttu-id="7425f-139">Rapporterar antalet objekt i data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7425f-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7425f-140">För närvarande tar den här parametern ingenting.</span><span class="sxs-lookup"><span data-stu-id="7425f-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7425f-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7425f-141">-ObjectId</span></span>
<span data-ttu-id="7425f-142">Objekt-ID för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="7425f-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="7425f-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7425f-143">-ServicePrincipalName</span></span>
<span data-ttu-id="7425f-144">Tjänstens SPN.</span><span class="sxs-lookup"><span data-stu-id="7425f-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7425f-145">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="7425f-145">-Skip</span></span>
<span data-ttu-id="7425f-146">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="7425f-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="7425f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7425f-147">CommonParameters</span></span>
<span data-ttu-id="7425f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7425f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7425f-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7425f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7425f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7425f-150">INPUTS</span></span>

### <span data-ttu-id="7425f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7425f-151">System.String</span></span>

### <span data-ttu-id="7425f-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7425f-152">System.Guid</span></span>

### <span data-ttu-id="7425f-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7425f-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7425f-154">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7425f-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="7425f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7425f-155">OUTPUTS</span></span>

### <span data-ttu-id="7425f-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7425f-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="7425f-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7425f-157">NOTES</span></span>

## <span data-ttu-id="7425f-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7425f-158">RELATED LINKS</span></span>

[<span data-ttu-id="7425f-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7425f-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="7425f-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7425f-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="7425f-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7425f-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="7425f-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7425f-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)
