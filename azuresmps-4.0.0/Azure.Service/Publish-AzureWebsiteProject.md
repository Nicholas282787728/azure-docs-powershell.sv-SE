---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099107"
---
# <span data-ttu-id="ad81c-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="ad81c-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="ad81c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad81c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad81c-103">Publicera ett Visual Studio-webbprojekt till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="ad81c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad81c-104">SYNTAX</span></span>

### <span data-ttu-id="ad81c-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="ad81c-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad81c-106">Underlag</span><span class="sxs-lookup"><span data-stu-id="ad81c-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad81c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad81c-107">DESCRIPTION</span></span>
<span data-ttu-id="ad81c-108">Publicera ett Visual Studio-webbprojekt till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="ad81c-109">Det kan antingen ta ett WebDeploy-paket och publicera direkt eller ta ett Visual Studio-webbprojekt, skapa projektet och publicera det.</span><span class="sxs-lookup"><span data-stu-id="ad81c-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="ad81c-110">Den kan också ersätta anslutnings strängarna i Web.config under publiceringen.</span><span class="sxs-lookup"><span data-stu-id="ad81c-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="ad81c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad81c-111">EXAMPLES</span></span>

### <span data-ttu-id="ad81c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad81c-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="ad81c-113">Skapa ett Visual Studio-webbprojekt med "debug"-konfiguration (d.v.s. använda Web.Debug.config) och publicera till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="ad81c-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ad81c-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="ad81c-115">Publicera en zip-fil på en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="ad81c-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ad81c-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="ad81c-117">Publicera en mapp för WebDeploy-paket till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="ad81c-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ad81c-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="ad81c-119">Skapa ett Visual Studio-webbprojekt och skriv över "DefaultConnection"-anslutnings strängen i Web.config och publicera till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="ad81c-120">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="ad81c-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="ad81c-121">Skapa ett Visual Studio-webbprojekt och skriv över "DefaultConnection"-anslutnings strängen i Web.config och publicera till en Microsoft Azure-webbplats med hjälp av WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="ad81c-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="ad81c-122">Observera att-DefaultConnection är en dynamisk parameter som läggs till genom att parsa Web.config.</span><span class="sxs-lookup"><span data-stu-id="ad81c-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="ad81c-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad81c-123">PARAMETERS</span></span>

### <span data-ttu-id="ad81c-124">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ad81c-124">-Configuration</span></span>
<span data-ttu-id="ad81c-125">Den konfiguration som används för att skapa webb programmet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ad81c-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ad81c-126">-ConnectionString</span></span>
<span data-ttu-id="ad81c-127">De anslutnings strängar som ska användas för distributionen.</span><span class="sxs-lookup"><span data-stu-id="ad81c-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="ad81c-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad81c-129">-Name</span></span>
<span data-ttu-id="ad81c-130">Webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="ad81c-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-131">-Paketera</span><span class="sxs-lookup"><span data-stu-id="ad81c-131">-Package</span></span>
<span data-ttu-id="ad81c-132">Mappen WebDeploy-paket för zip-filen i Visual Studio Web Application-projektet som ska publiceras.</span><span class="sxs-lookup"><span data-stu-id="ad81c-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad81c-133">-Profile</span></span>
<span data-ttu-id="ad81c-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ad81c-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad81c-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ad81c-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="ad81c-136">-ProjectFile</span></span>
<span data-ttu-id="ad81c-137">Visual Studio Web Application-projektet som ska publiceras.</span><span class="sxs-lookup"><span data-stu-id="ad81c-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="ad81c-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="ad81c-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="ad81c-140">-Slot</span></span>
<span data-ttu-id="ad81c-141">Namn på webbplats platsen.</span><span class="sxs-lookup"><span data-stu-id="ad81c-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-142">-Token</span><span class="sxs-lookup"><span data-stu-id="ad81c-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad81c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad81c-143">CommonParameters</span></span>
<span data-ttu-id="ad81c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad81c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad81c-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad81c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad81c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad81c-146">INPUTS</span></span>

## <span data-ttu-id="ad81c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad81c-147">OUTPUTS</span></span>

## <span data-ttu-id="ad81c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad81c-148">NOTES</span></span>

## <span data-ttu-id="ad81c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad81c-149">RELATED LINKS</span></span>

[<span data-ttu-id="ad81c-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad81c-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ad81c-151">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad81c-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="ad81c-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad81c-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="ad81c-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad81c-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


