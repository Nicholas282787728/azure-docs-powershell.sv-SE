---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923337"
---
# <span data-ttu-id="d4887-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d4887-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="d4887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4887-102">SYNOPSIS</span></span>
<span data-ttu-id="d4887-103">Hämtar en Azure Web App slot-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="d4887-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="d4887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4887-104">SYNTAX</span></span>

### <span data-ttu-id="d4887-105">S</span><span class="sxs-lookup"><span data-stu-id="d4887-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4887-106">S2</span><span class="sxs-lookup"><span data-stu-id="d4887-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4887-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4887-107">DESCRIPTION</span></span>
<span data-ttu-id="d4887-108">Cmdleten **Get-AzWebAppSlotPublishingProfile** hämtar webb program publicerings profilen för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="d4887-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="d4887-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4887-109">EXAMPLES</span></span>

### <span data-ttu-id="d4887-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4887-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="d4887-111">Det här kommandot får publicerings profilen i FTP-format för fack Slot001 som hör till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="d4887-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="d4887-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4887-112">PARAMETERS</span></span>

### <span data-ttu-id="d4887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4887-113">-DefaultProfile</span></span>
<span data-ttu-id="d4887-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4887-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4887-115">-Format</span><span class="sxs-lookup"><span data-stu-id="d4887-115">-Format</span></span>
<span data-ttu-id="d4887-116">Format</span><span class="sxs-lookup"><span data-stu-id="d4887-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4887-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4887-117">-Name</span></span>
<span data-ttu-id="d4887-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d4887-118">WebApp Name</span></span>

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

### <span data-ttu-id="d4887-119">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="d4887-119">-OutputFile</span></span>
<span data-ttu-id="d4887-120">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="d4887-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4887-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4887-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4887-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d4887-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d4887-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="d4887-123">-Slot</span></span>
<span data-ttu-id="d4887-124">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d4887-124">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4887-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d4887-125">-WebApp</span></span>
<span data-ttu-id="d4887-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d4887-126">WebApp Object</span></span>

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

### <span data-ttu-id="d4887-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4887-127">CommonParameters</span></span>
<span data-ttu-id="d4887-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4887-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4887-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4887-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4887-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4887-130">INPUTS</span></span>

### <span data-ttu-id="d4887-131">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d4887-131">Site</span></span>
<span data-ttu-id="d4887-132">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d4887-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d4887-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4887-133">OUTPUTS</span></span>

## <span data-ttu-id="d4887-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4887-134">NOTES</span></span>

## <span data-ttu-id="d4887-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4887-135">RELATED LINKS</span></span>

[<span data-ttu-id="d4887-136">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d4887-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="d4887-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4887-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d4887-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4887-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
