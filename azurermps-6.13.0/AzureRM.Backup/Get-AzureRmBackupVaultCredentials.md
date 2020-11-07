---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756703"
---
# <span data-ttu-id="c9eff-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="c9eff-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="c9eff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9eff-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eff-103">Laddar ned valv filen för autentiseringsuppgifter för ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="c9eff-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9eff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9eff-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9eff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9eff-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eff-106">Cmdleten **Get-AzureRmBackupVaultCredentials** laddar ned valvet för ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="c9eff-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>
<span data-ttu-id="c9eff-107">Vid säkerhets kopiering används en fil för valv för att ansluta en server till Azure Backup-valvet och registrera den.</span><span class="sxs-lookup"><span data-stu-id="c9eff-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="c9eff-108">Du måste registrera en server innan säkerhets kopiering kan skicka säkerhets kopior till valvet.</span><span class="sxs-lookup"><span data-stu-id="c9eff-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="c9eff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9eff-109">EXAMPLES</span></span>

## <span data-ttu-id="c9eff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-110">PARAMETERS</span></span>

### <span data-ttu-id="c9eff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eff-111">-DefaultProfile</span></span>
<span data-ttu-id="c9eff-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9eff-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9eff-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="c9eff-113">-TargetLocation</span></span>
<span data-ttu-id="c9eff-114">Anger mål Sök vägen där denna cmdlet lagrar valv filen för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="c9eff-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

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

### <span data-ttu-id="c9eff-115">-Valv</span><span class="sxs-lookup"><span data-stu-id="c9eff-115">-Vault</span></span>
<span data-ttu-id="c9eff-116">Anger det säkerhets kopierings valv som denna cmdlet hämtar en autentiseringsinformation för.</span><span class="sxs-lookup"><span data-stu-id="c9eff-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="c9eff-117">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c9eff-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eff-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eff-118">CommonParameters</span></span>
<span data-ttu-id="c9eff-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eff-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eff-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eff-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eff-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9eff-121">INPUTS</span></span>

### <span data-ttu-id="c9eff-122">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="c9eff-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="c9eff-123">Parametrar: valv (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9eff-123">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="c9eff-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9eff-124">OUTPUTS</span></span>

### <span data-ttu-id="c9eff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c9eff-125">System.String</span></span>
<span data-ttu-id="c9eff-126">Denna cmdlet returnerar namnet på filen för valv-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="c9eff-126">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="c9eff-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-127">NOTES</span></span>

## <span data-ttu-id="c9eff-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9eff-129">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c9eff-129">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


