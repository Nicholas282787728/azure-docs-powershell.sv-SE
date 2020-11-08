---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272386"
---
# <span data-ttu-id="927cd-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="927cd-101">Update-AzADApplication</span></span>

## <span data-ttu-id="927cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="927cd-102">SYNOPSIS</span></span>
<span data-ttu-id="927cd-103">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="927cd-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="927cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="927cd-104">SYNTAX</span></span>

### <span data-ttu-id="927cd-105">ApplicationObjectIdWithUpdateParamsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="927cd-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927cd-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="927cd-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927cd-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="927cd-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927cd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="927cd-108">DESCRIPTION</span></span>
<span data-ttu-id="927cd-109">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="927cd-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="927cd-110">Använd New-AzADAppCredential cmdlet för att uppdatera autentiseringsuppgifterna för det här programmet.</span><span class="sxs-lookup"><span data-stu-id="927cd-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="927cd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="927cd-111">EXAMPLES</span></span>

### <span data-ttu-id="927cd-112">Exempel 1 – uppdatera visnings namnet för ett program</span><span class="sxs-lookup"><span data-stu-id="927cd-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="927cd-113">Uppdaterar visnings namnet för programmet med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="927cd-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="927cd-114">Exempel 2 – uppdatera alla egenskaper för ett program</span><span class="sxs-lookup"><span data-stu-id="927cd-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="927cd-115">Uppdaterar egenskaperna för ett program med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 '.</span><span class="sxs-lookup"><span data-stu-id="927cd-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="927cd-116">Exempel 3 – uppdatera visnings namnet för ett program med hjälp av rör</span><span class="sxs-lookup"><span data-stu-id="927cd-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="927cd-117">Hämtar programmet med objekt-ID ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' och rör till cmdleten Update-AzADApplication för att uppdatera programmets visnings namn till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="927cd-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="927cd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="927cd-118">PARAMETERS</span></span>

### <span data-ttu-id="927cd-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="927cd-119">-ApplicationId</span></span>
<span data-ttu-id="927cd-120">Program-ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="927cd-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="927cd-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="927cd-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="927cd-122">Sant om programmet delas med andra klient organisationer; annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="927cd-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="927cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927cd-123">-DefaultProfile</span></span>
<span data-ttu-id="927cd-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="927cd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="927cd-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="927cd-125">-DisplayName</span></span>
<span data-ttu-id="927cd-126">Visnings namnet för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="927cd-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="927cd-127">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="927cd-127">-HomePage</span></span>
<span data-ttu-id="927cd-128">URL-adressen till programmets start sida.</span><span class="sxs-lookup"><span data-stu-id="927cd-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="927cd-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="927cd-129">-IdentifierUri</span></span>
<span data-ttu-id="927cd-130">URI: erna som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="927cd-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="927cd-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="927cd-131">-InputObject</span></span>
<span data-ttu-id="927cd-132">Det objekt som representerar det program som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="927cd-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="927cd-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="927cd-133">-ObjectId</span></span>
<span data-ttu-id="927cd-134">Objekt-ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="927cd-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927cd-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="927cd-135">-ReplyUrl</span></span>
<span data-ttu-id="927cd-136">Anger de URL-adresser som användarna skickar till för att logga in, eller vilka omdirigerings-URI som OAuth 2,0-auktoriseringsregler och åtkomsttoken skickas till.</span><span class="sxs-lookup"><span data-stu-id="927cd-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="927cd-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="927cd-137">-Confirm</span></span>
<span data-ttu-id="927cd-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="927cd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927cd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927cd-139">-WhatIf</span></span>
<span data-ttu-id="927cd-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="927cd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927cd-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="927cd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927cd-142">CommonParameters</span></span>
<span data-ttu-id="927cd-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927cd-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="927cd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927cd-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="927cd-145">INPUTS</span></span>

### <span data-ttu-id="927cd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="927cd-146">System.String</span></span>

### <span data-ttu-id="927cd-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="927cd-147">System.Guid</span></span>

### <span data-ttu-id="927cd-148">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="927cd-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="927cd-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="927cd-149">System.String[]</span></span>

### <span data-ttu-id="927cd-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="927cd-150">System.Boolean</span></span>

## <span data-ttu-id="927cd-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="927cd-151">OUTPUTS</span></span>

### <span data-ttu-id="927cd-152">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="927cd-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="927cd-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="927cd-153">NOTES</span></span>

## <span data-ttu-id="927cd-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="927cd-154">RELATED LINKS</span></span>
