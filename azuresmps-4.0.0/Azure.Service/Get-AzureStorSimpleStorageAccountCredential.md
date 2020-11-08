---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093277"
---
# <span data-ttu-id="7c7ca-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c7ca-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="7c7ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7ca-103">Hämtar autentiseringsuppgifter för lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="7c7ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c7ca-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c7ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7c7ca-106">Cmdleten **Get-AzureStorSimpleStorageAccountCredential** hämtar autentiseringsuppgifter för lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="7c7ca-107">Denna cmdlet hämtar alla **StorageAccountCredential** -objekt som har kon figurer ATS i tjänsten eller en namngiven **StorageAccountCredential**.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="7c7ca-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c7ca-108">EXAMPLES</span></span>

### <span data-ttu-id="7c7ca-109">Exempel 1: Hämta alla autentiseringsuppgifter för en resurs</span><span class="sxs-lookup"><span data-stu-id="7c7ca-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="7c7ca-110">Det här kommandot får alla tillgängliga autentiseringsuppgifter för lagrings konton för den aktuella resursen.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="7c7ca-111">Exempel 2: Hämta autentiseringsuppgifter för ett visst lagrings konto</span><span class="sxs-lookup"><span data-stu-id="7c7ca-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="7c7ca-112">Det här kommandot hämtar autentiseringsuppgifterna för lagrings kontot för lagrings kontot med namnet ContosoCloudStorage.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="7c7ca-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="7c7ca-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="7c7ca-114">-Profile</span></span>
<span data-ttu-id="7c7ca-115">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-115">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7c7ca-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c7ca-116">-StorageAccountName</span></span>
<span data-ttu-id="7c7ca-117">Anger namnet på det lagrings konto som du vill hämta autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7ca-118">CommonParameters</span></span>
<span data-ttu-id="7c7ca-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7ca-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7ca-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c7ca-121">INPUTS</span></span>

### <span data-ttu-id="7c7ca-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="7c7ca-122">None</span></span>

## <span data-ttu-id="7c7ca-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c7ca-123">OUTPUTS</span></span>

### <span data-ttu-id="7c7ca-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="7c7ca-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="7c7ca-125">Denna cmdlet returnerar ett **StorageAccountCredential** -objekt, om du anger parametern *StorageAccountName* eller om du inte anger den parametern, returnerar den ett **ilist \<StorageAccountCredential\>** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7c7ca-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="7c7ca-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c7ca-126">NOTES</span></span>

## <span data-ttu-id="7c7ca-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c7ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="7c7ca-128">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c7ca-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7c7ca-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c7ca-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7c7ca-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c7ca-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


