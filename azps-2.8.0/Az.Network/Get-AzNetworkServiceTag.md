---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: cbf01f50c72eef4d016754b063d0d10700553e3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918730"
---
# <span data-ttu-id="d26f6-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d26f6-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="d26f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d26f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d26f6-103">Hämtar listan över service tag information-resurser.</span><span class="sxs-lookup"><span data-stu-id="d26f6-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="d26f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d26f6-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d26f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d26f6-106">Cmdleten **Get-AzNetworkServiceTag** hämtar listan med information om tjänst märknings resurser.</span><span class="sxs-lookup"><span data-stu-id="d26f6-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="d26f6-107">Observera att den Azure region information du anger kommer att användas som referens för versionen (inte som ett filter baserat på plats).</span><span class="sxs-lookup"><span data-stu-id="d26f6-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="d26f6-108">Till exempel om du anger `-Location eastus2` att du vill få en lista med service märken med uppgifter om prefix i alla regioner, men begränsat till det moln som ditt abonnemang tillhör (t. ex. offentlig, amerikansk regering, Kina eller Tyskland).</span><span class="sxs-lookup"><span data-stu-id="d26f6-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="d26f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d26f6-109">EXAMPLES</span></span>

### <span data-ttu-id="d26f6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d26f6-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="d26f6-111">Kommandot hämtar listan med information om tjänst märknings resurser och lagrar den i variabelt format `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d26f6-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="d26f6-112">Exempel 2: Hämta alla adressprefix för AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d26f6-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="d26f6-113">Det första kommandot får listan med information om tjänst märknings resurser och lagrar den i variabeln `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d26f6-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d26f6-114">Det andra kommandot filtrerar listan för att välja informations resurs för SQL.</span><span class="sxs-lookup"><span data-stu-id="d26f6-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="d26f6-115">Exempel 3: Hämta lagrings information om tjänst tag gen för västra USA 2</span><span class="sxs-lookup"><span data-stu-id="d26f6-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="d26f6-116">Det första kommandot får listan med information om tjänst märknings resurser och lagrar den i variabeln `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d26f6-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d26f6-117">Följande kommandon visar olika sätt att filtrera listan för att välja service tag-information för lagrings utrymme i västra USA 2.</span><span class="sxs-lookup"><span data-stu-id="d26f6-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="d26f6-118">Exempel 4: Hämta alla globala service märknings resurser</span><span class="sxs-lookup"><span data-stu-id="d26f6-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="d26f6-119">Det första kommandot får listan med information om tjänst märknings resurser och lagrar den i variabeln `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d26f6-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d26f6-120">Det andra kommandot filtrerar listan för att välja endast dem utan att ange region.</span><span class="sxs-lookup"><span data-stu-id="d26f6-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="d26f6-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d26f6-121">PARAMETERS</span></span>

### <span data-ttu-id="d26f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26f6-122">-DefaultProfile</span></span>
<span data-ttu-id="d26f6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d26f6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26f6-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="d26f6-124">-Location</span></span>
<span data-ttu-id="d26f6-125">Platsen som ska användas som referens för versionen (inte som ett filter baserat på plats) får du en lista över service märken med information om uppgifter i alla regioner, men begränsat till det moln som ditt abonnemang tillhör).</span><span class="sxs-lookup"><span data-stu-id="d26f6-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d26f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26f6-126">CommonParameters</span></span>
<span data-ttu-id="d26f6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26f6-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d26f6-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26f6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d26f6-129">INPUTS</span></span>

### <span data-ttu-id="d26f6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d26f6-130">System.String</span></span>

## <span data-ttu-id="d26f6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d26f6-131">OUTPUTS</span></span>

### <span data-ttu-id="d26f6-132">Microsoft. Azure. commands. Networks. Models. PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d26f6-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="d26f6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d26f6-133">NOTES</span></span>

## <span data-ttu-id="d26f6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d26f6-134">RELATED LINKS</span></span>
