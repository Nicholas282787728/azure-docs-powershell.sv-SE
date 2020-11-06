---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575748"
---
# <span data-ttu-id="57061-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="57061-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="57061-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57061-102">SYNOPSIS</span></span>
<span data-ttu-id="57061-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="57061-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57061-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57061-104">SYNTAX</span></span>

### <span data-ttu-id="57061-105">S</span><span class="sxs-lookup"><span data-stu-id="57061-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57061-106">S2</span><span class="sxs-lookup"><span data-stu-id="57061-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57061-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57061-107">DESCRIPTION</span></span>
<span data-ttu-id="57061-108">Cmdleten **Get-AzureRmWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="57061-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="57061-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57061-109">EXAMPLES</span></span>

### <span data-ttu-id="57061-110">9.1</span><span class="sxs-lookup"><span data-stu-id="57061-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="57061-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="57061-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="57061-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57061-112">PARAMETERS</span></span>

### <span data-ttu-id="57061-113">-Format</span><span class="sxs-lookup"><span data-stu-id="57061-113">-Format</span></span>
<span data-ttu-id="57061-114">Format</span><span class="sxs-lookup"><span data-stu-id="57061-114">Format</span></span>

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

### <span data-ttu-id="57061-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="57061-115">-Name</span></span>
<span data-ttu-id="57061-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="57061-116">WebApp Name</span></span>

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

### <span data-ttu-id="57061-117">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="57061-117">-OutputFile</span></span>
<span data-ttu-id="57061-118">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="57061-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57061-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57061-119">-ResourceGroupName</span></span>
<span data-ttu-id="57061-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="57061-120">Resource Group Name</span></span>

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

### <span data-ttu-id="57061-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="57061-121">-WebApp</span></span>
<span data-ttu-id="57061-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="57061-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57061-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57061-123">-DefaultProfile</span></span>
<span data-ttu-id="57061-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57061-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57061-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57061-125">CommonParameters</span></span>
<span data-ttu-id="57061-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57061-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57061-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57061-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57061-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57061-128">INPUTS</span></span>

### <span data-ttu-id="57061-129">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="57061-129">Site</span></span>
<span data-ttu-id="57061-130">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="57061-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="57061-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57061-131">OUTPUTS</span></span>

## <span data-ttu-id="57061-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57061-132">NOTES</span></span>

## <span data-ttu-id="57061-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57061-133">RELATED LINKS</span></span>

[<span data-ttu-id="57061-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="57061-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="57061-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="57061-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


