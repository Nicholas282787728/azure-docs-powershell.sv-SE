---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 56b3c942fe033f32b18c19ec669b19d87397c5bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926322"
---
# <span data-ttu-id="e5e80-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e5e80-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="e5e80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5e80-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e80-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="e5e80-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="e5e80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5e80-104">SYNTAX</span></span>

### <span data-ttu-id="e5e80-105">S</span><span class="sxs-lookup"><span data-stu-id="e5e80-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5e80-106">S2</span><span class="sxs-lookup"><span data-stu-id="e5e80-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e80-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5e80-107">DESCRIPTION</span></span>
<span data-ttu-id="e5e80-108">Cmdleten **Get-AzWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="e5e80-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="e5e80-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5e80-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e80-110">9.1</span><span class="sxs-lookup"><span data-stu-id="e5e80-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="e5e80-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="e5e80-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="e5e80-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5e80-112">PARAMETERS</span></span>

### <span data-ttu-id="e5e80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e80-113">-DefaultProfile</span></span>
<span data-ttu-id="e5e80-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e80-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e80-115">-Format</span><span class="sxs-lookup"><span data-stu-id="e5e80-115">-Format</span></span>
<span data-ttu-id="e5e80-116">Format</span><span class="sxs-lookup"><span data-stu-id="e5e80-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e80-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="e5e80-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="e5e80-118">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="e5e80-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="e5e80-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5e80-119">-Name</span></span>
<span data-ttu-id="e5e80-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="e5e80-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e80-121">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="e5e80-121">-OutputFile</span></span>
<span data-ttu-id="e5e80-122">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="e5e80-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e80-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5e80-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e5e80-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e80-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e5e80-125">-WebApp</span></span>
<span data-ttu-id="e5e80-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="e5e80-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e80-127">CommonParameters</span></span>
<span data-ttu-id="e5e80-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e80-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e80-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e80-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5e80-130">INPUTS</span></span>

### <span data-ttu-id="e5e80-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e80-131">System.String</span></span>

### <span data-ttu-id="e5e80-132">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e5e80-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e5e80-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5e80-133">OUTPUTS</span></span>

### <span data-ttu-id="e5e80-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e80-134">System.String</span></span>

## <span data-ttu-id="e5e80-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5e80-135">NOTES</span></span>

## <span data-ttu-id="e5e80-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5e80-136">RELATED LINKS</span></span>

[<span data-ttu-id="e5e80-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e5e80-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="e5e80-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5e80-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


