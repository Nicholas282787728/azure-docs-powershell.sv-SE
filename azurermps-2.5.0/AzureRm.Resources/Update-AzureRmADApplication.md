---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: bf9f993724de9ed20587a3f4ca136c3531689401
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929601"
---
# <span data-ttu-id="a4402-101">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a4402-101">Update-AzureRmADApplication</span></span>

## <span data-ttu-id="a4402-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4402-102">SYNOPSIS</span></span>
<span data-ttu-id="a4402-103">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="a4402-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4402-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4402-104">SYNTAX</span></span>

### <span data-ttu-id="a4402-105">ApplicationObjectIdWithUpdateParamsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a4402-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzureRmADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4402-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4402-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4402-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4402-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4402-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4402-108">DESCRIPTION</span></span>
<span data-ttu-id="a4402-109">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="a4402-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="a4402-110">Använd New-AzureRmADAppCredential cmdlet för att uppdatera autentiseringsuppgifterna för det här programmet.</span><span class="sxs-lookup"><span data-stu-id="a4402-110">To update the credentials associated with this application, please use the New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="a4402-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4402-111">EXAMPLES</span></span>

### <span data-ttu-id="a4402-112">Exempel 1 – uppdatera visnings namnet för ett program</span><span class="sxs-lookup"><span data-stu-id="a4402-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="a4402-113">Uppdaterar visnings namnet för programmet med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="a4402-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a4402-114">Exempel 2 – uppdatera alla egenskaper för ett program</span><span class="sxs-lookup"><span data-stu-id="a4402-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="a4402-115">Uppdaterar egenskaperna för ett program med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 '.</span><span class="sxs-lookup"><span data-stu-id="a4402-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="a4402-116">Exempel 3 – uppdatera visnings namnet för ett program med hjälp av rör</span><span class="sxs-lookup"><span data-stu-id="a4402-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzureRmADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="a4402-117">Hämtar programmet med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' och rör till cmdleten Update-AzureRmADApplication för att uppdatera programmets visnings namn till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a4402-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzureRmADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="a4402-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4402-118">PARAMETERS</span></span>

### <span data-ttu-id="a4402-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a4402-119">-ApplicationId</span></span>
<span data-ttu-id="a4402-120">Program-ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a4402-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="a4402-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="a4402-122">Sant om programmet delas med andra klient organisationer; annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4402-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4402-123">-DefaultProfile</span></span>
<span data-ttu-id="a4402-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4402-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4402-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4402-125">-DisplayName</span></span>
<span data-ttu-id="a4402-126">Visnings namnet för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a4402-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-127">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="a4402-127">-HomePage</span></span>
<span data-ttu-id="a4402-128">URL-adressen till programmets start sida.</span><span class="sxs-lookup"><span data-stu-id="a4402-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="a4402-129">-IdentifierUri</span></span>
<span data-ttu-id="a4402-130">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="a4402-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4402-131">-InputObject</span></span>
<span data-ttu-id="a4402-132">Det objekt som representerar det program som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a4402-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a4402-133">-ObjectId</span></span>
<span data-ttu-id="a4402-134">Objekt-ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a4402-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="a4402-135">-ReplyUrl</span></span>
<span data-ttu-id="a4402-136">Anger de URL-adresser som användarna skickar till för att logga in, eller vilka omdirigerings-URI som OAuth 2,0-auktoriseringsregler och åtkomsttoken skickas till.</span><span class="sxs-lookup"><span data-stu-id="a4402-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4402-137">-Confirm</span></span>
<span data-ttu-id="a4402-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4402-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4402-139">-WhatIf</span></span>
<span data-ttu-id="a4402-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4402-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4402-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4402-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4402-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4402-142">CommonParameters</span></span>
<span data-ttu-id="a4402-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4402-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4402-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4402-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4402-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4402-145">INPUTS</span></span>

### <span data-ttu-id="a4402-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a4402-146">System.Guid</span></span>

### <span data-ttu-id="a4402-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a4402-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="a4402-148">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4402-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a4402-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a4402-149">System.String</span></span>

### <span data-ttu-id="a4402-150">System. string []</span><span class="sxs-lookup"><span data-stu-id="a4402-150">System.String[]</span></span>

### <span data-ttu-id="a4402-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4402-151">System.Boolean</span></span>

## <span data-ttu-id="a4402-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4402-152">OUTPUTS</span></span>

### <span data-ttu-id="a4402-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a4402-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a4402-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4402-154">NOTES</span></span>

## <span data-ttu-id="a4402-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4402-155">RELATED LINKS</span></span>
