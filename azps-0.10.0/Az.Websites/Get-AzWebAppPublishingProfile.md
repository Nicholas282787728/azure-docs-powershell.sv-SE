---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923346"
---
# <span data-ttu-id="3e55c-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3e55c-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="3e55c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e55c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e55c-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="3e55c-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="3e55c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e55c-104">SYNTAX</span></span>

### <span data-ttu-id="3e55c-105">S</span><span class="sxs-lookup"><span data-stu-id="3e55c-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e55c-106">S2</span><span class="sxs-lookup"><span data-stu-id="3e55c-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e55c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e55c-107">DESCRIPTION</span></span>
<span data-ttu-id="3e55c-108">Cmdleten **Get-AzWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="3e55c-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="3e55c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e55c-109">EXAMPLES</span></span>

### <span data-ttu-id="3e55c-110">9.1</span><span class="sxs-lookup"><span data-stu-id="3e55c-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="3e55c-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="3e55c-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="3e55c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e55c-112">PARAMETERS</span></span>

### <span data-ttu-id="3e55c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e55c-113">-DefaultProfile</span></span>
<span data-ttu-id="3e55c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e55c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-115">-Format</span><span class="sxs-lookup"><span data-stu-id="3e55c-115">-Format</span></span>
<span data-ttu-id="3e55c-116">Format</span><span class="sxs-lookup"><span data-stu-id="3e55c-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e55c-117">-Name</span></span>
<span data-ttu-id="3e55c-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="3e55c-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-119">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="3e55c-119">-OutputFile</span></span>
<span data-ttu-id="3e55c-120">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="3e55c-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e55c-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e55c-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3e55c-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3e55c-123">-WebApp</span></span>
<span data-ttu-id="3e55c-124">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="3e55c-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e55c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e55c-125">CommonParameters</span></span>
<span data-ttu-id="3e55c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e55c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e55c-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e55c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e55c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e55c-128">INPUTS</span></span>

### <span data-ttu-id="3e55c-129">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="3e55c-129">Site</span></span>
<span data-ttu-id="3e55c-130">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3e55c-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3e55c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e55c-131">OUTPUTS</span></span>

## <span data-ttu-id="3e55c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e55c-132">NOTES</span></span>

## <span data-ttu-id="3e55c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e55c-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e55c-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e55c-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="3e55c-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3e55c-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


