---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577839"
---
# <span data-ttu-id="e2bbc-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="e2bbc-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="e2bbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="e2bbc-103">Hämtar ett tids periodiska valv för Server.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2bbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2bbc-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2bbc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="e2bbc-106">Cmdleten **Get-AzureRmSqlServerBackupLongTermRetentionVault** hämtar det långsiktiga bevarande valvet för den här servern.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="e2bbc-107">Valvet är en Azure Backup-resurs som används för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="e2bbc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2bbc-108">EXAMPLES</span></span>

## <span data-ttu-id="e2bbc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2bbc-109">PARAMETERS</span></span>

### <span data-ttu-id="e2bbc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2bbc-110">-DefaultProfile</span></span>
<span data-ttu-id="e2bbc-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2bbc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2bbc-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2bbc-112">-ResourceGroupName</span></span>
<span data-ttu-id="e2bbc-113">Anger namnet på den resurs grupp som innehåller servern.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-113">Specifies the name of the resource group that contains the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2bbc-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2bbc-114">-ServerName</span></span>
<span data-ttu-id="e2bbc-115">Anger den server som den här cmdleten får ett valv för.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-115">Specifies the server for which this cmdlet gets a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2bbc-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2bbc-116">-Confirm</span></span>
<span data-ttu-id="e2bbc-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2bbc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2bbc-118">-WhatIf</span></span>
<span data-ttu-id="e2bbc-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2bbc-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2bbc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2bbc-121">CommonParameters</span></span>
<span data-ttu-id="e2bbc-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2bbc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2bbc-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2bbc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2bbc-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2bbc-124">INPUTS</span></span>

### <span data-ttu-id="e2bbc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e2bbc-125">System.String</span></span>

## <span data-ttu-id="e2bbc-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2bbc-126">OUTPUTS</span></span>

### <span data-ttu-id="e2bbc-127">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="e2bbc-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="e2bbc-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2bbc-128">NOTES</span></span>

## <span data-ttu-id="e2bbc-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2bbc-129">RELATED LINKS</span></span>

[<span data-ttu-id="e2bbc-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="e2bbc-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="e2bbc-131">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e2bbc-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

