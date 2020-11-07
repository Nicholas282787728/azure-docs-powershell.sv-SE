---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756837"
---
# <span data-ttu-id="2eb3d-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2eb3d-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="2eb3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb3d-103">Hämtar ett tids periodiska valv för Server.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eb3d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eb3d-105">DESCRIPTION</span></span>
<span data-ttu-id="2eb3d-106">Cmdleten **Get-AzureRmSqlServerBackupLongTermRetentionVault** hämtar det långsiktiga bevarande valvet för den här servern.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="2eb3d-107">Valvet är en Azure Backup-resurs som används för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="2eb3d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eb3d-108">EXAMPLES</span></span>

## <span data-ttu-id="2eb3d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eb3d-109">PARAMETERS</span></span>

### <span data-ttu-id="2eb3d-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb3d-110">-ResourceGroupName</span></span>
<span data-ttu-id="2eb3d-111">Anger namnet på den resurs grupp som innehåller servern.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="2eb3d-112">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2eb3d-112">-ServerName</span></span>
<span data-ttu-id="2eb3d-113">Anger den server som den här cmdleten får ett valv för.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="2eb3d-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2eb3d-114">-Confirm</span></span>
<span data-ttu-id="2eb3d-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb3d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb3d-116">-WhatIf</span></span>
<span data-ttu-id="2eb3d-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb3d-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb3d-119">-DefaultProfile</span></span>
<span data-ttu-id="2eb3d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eb3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb3d-121">CommonParameters</span></span>
<span data-ttu-id="2eb3d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb3d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb3d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb3d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eb3d-124">INPUTS</span></span>

## <span data-ttu-id="2eb3d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eb3d-125">OUTPUTS</span></span>

## <span data-ttu-id="2eb3d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eb3d-126">NOTES</span></span>

## <span data-ttu-id="2eb3d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eb3d-127">RELATED LINKS</span></span>

[<span data-ttu-id="2eb3d-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2eb3d-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="2eb3d-129">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="2eb3d-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

