---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929185"
---
# <span data-ttu-id="5fe68-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5fe68-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="5fe68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fe68-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe68-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="5fe68-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fe68-104">SYNTAX</span></span>

### <span data-ttu-id="5fe68-105">S</span><span class="sxs-lookup"><span data-stu-id="5fe68-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe68-106">S2</span><span class="sxs-lookup"><span data-stu-id="5fe68-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe68-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fe68-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe68-108">Cmdleten **Get-AzureRmWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="5fe68-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="5fe68-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fe68-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe68-110">9.1</span><span class="sxs-lookup"><span data-stu-id="5fe68-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="5fe68-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="5fe68-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="5fe68-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fe68-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe68-113">-DefaultProfile</span></span>
<span data-ttu-id="5fe68-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe68-115">-Format</span><span class="sxs-lookup"><span data-stu-id="5fe68-115">-Format</span></span>
<span data-ttu-id="5fe68-116">Format</span><span class="sxs-lookup"><span data-stu-id="5fe68-116">Format</span></span>

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

### <span data-ttu-id="5fe68-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fe68-117">-Name</span></span>
<span data-ttu-id="5fe68-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5fe68-118">WebApp Name</span></span>

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

### <span data-ttu-id="5fe68-119">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="5fe68-119">-OutputFile</span></span>
<span data-ttu-id="5fe68-120">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="5fe68-120">Output File</span></span>

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

### <span data-ttu-id="5fe68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe68-121">-ResourceGroupName</span></span>
<span data-ttu-id="5fe68-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5fe68-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5fe68-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5fe68-123">-WebApp</span></span>
<span data-ttu-id="5fe68-124">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="5fe68-124">WebApp Object</span></span>

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

### <span data-ttu-id="5fe68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe68-125">CommonParameters</span></span>
<span data-ttu-id="5fe68-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe68-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe68-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe68-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fe68-128">INPUTS</span></span>

### <span data-ttu-id="5fe68-129">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="5fe68-129">Site</span></span>
<span data-ttu-id="5fe68-130">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5fe68-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5fe68-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fe68-131">OUTPUTS</span></span>

## <span data-ttu-id="5fe68-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fe68-132">NOTES</span></span>

## <span data-ttu-id="5fe68-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fe68-133">RELATED LINKS</span></span>

[<span data-ttu-id="5fe68-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5fe68-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5fe68-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5fe68-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


