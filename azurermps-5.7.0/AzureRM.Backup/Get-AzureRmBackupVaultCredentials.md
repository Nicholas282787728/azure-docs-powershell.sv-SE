---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756817"
---
# <span data-ttu-id="7bbf3-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="7bbf3-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="7bbf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbf3-103">Laddar ned valv filen för autentiseringsuppgifter för ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bbf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bbf3-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bbf3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bbf3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bbf3-106">Cmdleten **Get-AzureRmBackupVaultCredentials** laddar ned valvet för ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="7bbf3-107">Vid säkerhets kopiering används en fil för valv för att ansluta en server till Azure Backup-valvet och registrera den.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="7bbf3-108">Du måste registrera en server innan säkerhets kopiering kan skicka säkerhets kopior till valvet.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="7bbf3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bbf3-109">EXAMPLES</span></span>

## <span data-ttu-id="7bbf3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bbf3-110">PARAMETERS</span></span>

### <span data-ttu-id="7bbf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbf3-111">-DefaultProfile</span></span>
<span data-ttu-id="7bbf3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7bbf3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bbf3-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="7bbf3-113">-TargetLocation</span></span>
<span data-ttu-id="7bbf3-114">Anger mål Sök vägen där denna cmdlet lagrar valv filen för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbf3-115">-Valv</span><span class="sxs-lookup"><span data-stu-id="7bbf3-115">-Vault</span></span>
<span data-ttu-id="7bbf3-116">Anger det säkerhets kopierings valv som denna cmdlet hämtar en autentiseringsinformation för.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="7bbf3-117">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbf3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbf3-118">CommonParameters</span></span>
<span data-ttu-id="7bbf3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbf3-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bbf3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbf3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bbf3-121">INPUTS</span></span>

### <span data-ttu-id="7bbf3-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="7bbf3-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="7bbf3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bbf3-123">OUTPUTS</span></span>

### <span data-ttu-id="7bbf3-124">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="7bbf3-124">String</span></span>
<span data-ttu-id="7bbf3-125">Denna cmdlet returnerar namnet på filen för valv-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="7bbf3-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="7bbf3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bbf3-126">NOTES</span></span>

## <span data-ttu-id="7bbf3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bbf3-127">RELATED LINKS</span></span>

[<span data-ttu-id="7bbf3-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7bbf3-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


